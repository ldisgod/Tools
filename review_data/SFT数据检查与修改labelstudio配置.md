<View className="root">
  <Style>
    html, body {
  height: 100%;
  margin: 0;
  padding: 0;
  overflow: hidden; /* 确保页面没有滚动条 */
}

    .root {
      font-family: 'Roboto', sans-serif;
      line-height: 1.6;
      background-color: #f0f0f0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 86vh;
      overflow: hidden;
    }
    .container {
      display: flex;
      justify-content: space-between;
      margin: 0 auto;
      padding: 20px;
      background-color: #ffffff;
      border-radius: 5px;
      box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1), 0 6px 20px 0 rgba(0, 0, 0, 0.1);
      width: 100%;
      height: 100%;
    overflow: hidden;
    }
    .instruction {
      flex-basis: 49%;
      padding: 20px;
      background-color: #0084ff;
      color: #ffffff;
      border-radius: 5px;
      box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.1), 0 3px 10px 0 rgba(0, 0, 0, 0.1);
      overflow: auto;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    .output-input {
      flex-basis: 49%;
      padding: 20px;
      background-color: rgba(44, 62, 80, 0.9);
      color: #ffffff;
      border-radius: 5px;
      box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.1), 0 3px 10px 0 rgba(0, 0, 0, 0.1);
      border: none;
      font-family: 'Roboto', sans-serif;
      font-size: 16px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      height: 100%;
    }
    .output-input textarea {
      width: 100%;
      height: 100%;
      background-color: transparent;
      border: none;
      color: #ffffff;
      font-family: 'Roboto', sans-serif;
      font-size: 16px;
      outline: none;
      resize: none;
      overflow: auto;
      white-space: pre-wrap;
      flex-grow: 1;
    }
    .output-input textarea:focus {
      outline: none;
    }
    .output-input textarea:hover {
      background-color: rgba(52, 73, 94, 0.9);
      cursor: text;
      transition: all 0.3s ease;
    }
    .lsf-richtext__line:hover {
      background: unset;
    }
  </Style>
  <View className="container">
    <View className="instruction">
      <Text name="instruction" value="$instruction" />
    </View>
    <View className="output-input">
      <TextArea name="output" toName="instruction"
                value="$output"
                maxSubmissions="1" required="true"
                requiredMessage="You must provide the response to the instruction"
                placeholder="Type your answer here..."
                rows="40" 
      />
    </View>
  </View>
</View>

<!-- {"data" : {
  "instruction": "Some instruction text 一些说明文字",
  "output": "Some output text"
}} -->