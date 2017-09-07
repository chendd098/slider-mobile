# slider-mobile
this is slider
222222222
555555555

```source _trigger2
import React, { Component } from 'react';
import { Calendar,Trigger } from 'beyond-datetime';

class App extends Component {

	constructor(props){
		super(props)
		this.state = {
			date : null
		}
	}

	handlerChange(date){
		this.setState((state, props) => ({date}))
	}

	render(){
		return (
			<div>
				<Trigger target={<Calendar date={this.state.date} onConfirm={this.handlerChange.bind(this)} />}>
					<input type="text" value={this.state.date ? this.state.date.format('YYYY.MM.DD') : '' } />
				</Trigger>
			</div>
		)
	}
}

```

```render

<Display  name="输入框选择" >
    <Item key="1" code={_trigger2} state="日期">
        <div><TriggerExample2  /></div>
    </Item>
    <Item key="0" code={_trigger} state="日期时间">
        <div><TriggerExample  /></div>
    </Item>
</Display>
```
