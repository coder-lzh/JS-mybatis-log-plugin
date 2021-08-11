<!DOCTYPE html>
<html lang="ch-zn">
<head>
    <meta charset="utf-8">
    <title></title>
    <script type="text/javascript">

        function multiTransefer(inputText) {
            document.getElementById('logAfterId').value = '';
            // 将传入的字符串根据MyBatis的标识拆分成数组
            var mybatisSQLTexts = [];

            while (inputText.lastIndexOf('Preparing: ') > -1) {
                // 因为是从尾部截取，所以需要从数组的头部添加
                mybatisSQLTexts.unshift(inputText.substring(inputText.lastIndexOf('Preparing: ')));

                inputText = inputText.substring(0, inputText.lastIndexOf('Preparing: '));
            }
            console.log(mybatisSQLTexts);

            // 将数组中的字符串挨个处理，以数组形式返回
            for (var i = 0; i < mybatisSQLTexts.length; i++) {
                parseSql(mybatisSQLTexts[i]);
            }
        }

        // 单句的问号生成SQL
        function parseSql(textVa) {
            // 获取带问号的SQL语句
            var statementStartIndex = textVa.indexOf('Preparing: ');
            var statementEndIndex = textVa.length - 1;
            for (var i = statementStartIndex; i < textVa.length; i++) {
                if (textVa[i] === "\n") {
                    statementEndIndex = i;
                    break;
                }
            }
            var statementStr = textVa.substring(statementStartIndex + "Preparing: ".length, statementEndIndex);
            // console.log(statementStr);
            //获取参数
            var parametersStartIndex = textVa.indexOf('Parameters: ');
            var parametersEndIndex = textVa.length - 1;
            for (var i = parametersStartIndex; i < textVa.length; i++) {
                if (textVa[i] === "\n") {
                    parametersEndIndex = i;
                    break;
                } else {
                    // console.log(textVa[i]);
                }
            }
            var parametersStr = textVa.substring(parametersStartIndex + "Parameters: ".length, parametersEndIndex+1);
            parametersStr = parametersStr.split(",");
            // console.log(parametersStr);
            for (var i = 0; i < parametersStr.length; i++) {
                // 如果数据中带括号将使用其他逻辑
                tempStr = parametersStr[i].substring(0, parametersStr[i].lastIndexOf("("));
                // 获取括号中内容
                typeStr = parametersStr[i].substring(parametersStr[i].lastIndexOf("(") + 1, parametersStr[i].lastIndexOf(")"));
                // 如果为字符类型
                if (typeStr === "String" || typeStr === "Timestamp" || typeStr === "Date") {
                    statementStr = statementStr.replace("?", "'" + tempStr.trim() + "'");
                } else {
                    // 数值类型
                    statementStr = statementStr.replace("?", tempStr.trim());
                }
            }
            // console.log(statementStr);
            document.getElementById("logAfterId").value += '\n\n\n';
            document.getElementById("logAfterId").value += statementStr;
            return textVa;
        }

        function clearContent() {
            document.getElementById('logBeforeId').value = '';
            document.getElementById('logAfterId').value = '';
        }
    </script>
</head>
<body>
<textarea style="width:40%;"  name="logBefore" id="logBeforeId" rows="40" placeholder="转换前的log"></textarea>
<button style="width:60px" type="submit" onclick="multiTransefer(document.getElementById('logBeforeId').value)">转换</button>
<button style="width:60px" type="input" onclick="clearContent()">清除</button>
<textarea style="width:40%;" name="logAfter" id="logAfterId" rows="40" placeholder="转换后的SQL"></textarea>
</body>
</html>
