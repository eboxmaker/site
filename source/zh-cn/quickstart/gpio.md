title:  ͨ�������������
---
��Box���� Hexo ���������ض��ļ����е��ļ����������� Hexo �������� Box���ֱ��� `hexo.source` �� `hexo.theme`��ǰ�����ڴ��� `source` �ļ��У����������ڴ��������ļ��С�

## �����ļ�

Box �ṩ�����ַ����������ļ���`process`, `watch`��ǰ�����������ļ����ڵ������ļ��������߳���ִ�� `process` ���⣬������������ļ��䶯��

``` js
box.process().then(function(){
  // ...
});

box.watch().then(function(){
  // ֮��ɵ��� box.unwatch()��ֹͣ�����ļ�
});
```

## �ȶ�·��

Box �ṩ�˶��ֱȶ�·����ģʽ����������ʹ��������ʽ��regular expression��������������һ�������� Express ��·���ַ��������磺

``` plain
posts/:id => posts/89
posts/*path => posts/2015/title
```

�������Բο� [util.Pattern] �Ի�ø�����Ϣ��

## ��������Processor��

��������Processor���� Box �зǳ���Ҫ��Ԫ�أ������ڴ����ļ���������ʹ��������·���Ա������Ƹô�������Ҫ������ļ����͡�ʹ�� `addProcessor` ����Ӵ�������

``` js
box.addProcessor('posts/:id', function(file){
  //
});
```

Box �ڴ���ʱ���Ŀǰ������ļ����ݣ�`file`��������������������ͨ���˲�����ø��ļ������ݡ�

���� | ����
--- | ---
`source` | �ļ�����·��
`path` | �ļ������ Box ��·��
`type` | �ļ����͡��� `create`, `update`, `skip`, `delete`��
`params` | ��·���Ա���ȡ�õ���Ϣ

Box ���ṩ��һЩ���������������ֶ������ļ� I/O��

���� | ����
--- | ---
`read` | ��ȡ�ļ�
`readSync` | ͬ����ȡ�ļ�
`stat` | ��ȡ�ļ�״̬
`statSync` | ͬ����ȡ�ļ�״̬
`render` | ��Ⱦ�ļ�
`renderSync` | ͬ����Ⱦ�ļ�

[util.Pattern]: https://github.com/hexojs/hexo-util#patternrule