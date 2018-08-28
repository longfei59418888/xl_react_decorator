
<pre>
<code>


import { defaultProps , loading, login, connect, setTitle} from 'src/decorators'

//设置标题
@setTitle('test')

// 设置默认的 props
@defaultProps({select:false})

// react-redux connect
@connect(['userInfo'],actions)

// 延时加载组件
@loading(async (props,state)=>{
    let userinfo = props.getUserInfo()
    await Promise.all([userinfo,SwitchTabs]);
})

// render 执行函数
@login(()=>{

    // 返回true 正常
    return true
})
export default class Btn extends React.Component{
    componentDidMount(){
       // loading 加载数据的存储数组
       this.state.load
    }
    // 自动绑定this
    @autobind
    change(){
        if(this.props.change) this.props.change(!this.state.select)
        this.setState({
            select:!this.state.select
        })
    }
}


</code>
</pre>