---
title: 'switch 語句 (Urlmon.dll) '
description: 將控制權傳輸至切換主體內的不同語句區塊（視選取器的值而定）。
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- switch 語句 HLSL
topic_type:
- apiref
api_name:
- switch Statement
api_location:
- urlmon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8527853bf88b073f3505f4b4170ff6165f7f9aa7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477484"
---
# <a name="switch-statement"></a>switch 陳述式

將控制權傳輸至切換主體內的不同語句區塊（視選取器的值而定）。


\[*屬性* \]切換 (*選取器*) {case 0： { *StatementBlock*;}  折  案例1： { *StatementBlock*;}  折  案例 n： { *StatementBlock*;}  折  預設值： { *StatementBlock*;}  折



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*屬性*
</dt> <dd>

可控制如何編譯語句的選擇性參數。 未指定任何屬性時，編譯器可能會使用硬體參數或發出一系列的 **if** 語句。




| 屬性 | 描述 | 
|-----------|-------------|
| 扁平化 | 將語句編譯為一系列的 <strong>if</strong> 語句，每個語句都有壓 <strong>平</strong> 合併屬性。 | 
| 分支 | 將語句編譯為一系列的 <strong>if</strong> 語句，其中每個語句都有 <strong>分支</strong> 屬性。<blockquote>[!Note]<br />當您使用 <a href="dx-graphics-hlsl-sm2.md">著色器模型</a> 2.X 或 <a href="dx-graphics-hlsl-sm3.md">著色器模型 3.0</a>時，每次使用動態分支都會耗用資源。 因此，如果您在以這些設定檔為目標時，過度使用動態分支，您可能會收到編譯錯誤。</blockquote><br /> | 
| forcecase | 在硬體中強制執行 switch 語句。<blockquote>[!Note]<br />需要 <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">功能層級</a> 10_0 或更新版本的硬體。</blockquote><br /> | 
| call | 交換器中個別案例的內文將會移至硬體副程式，而參數將會是一連串的副程式呼叫。<blockquote>[!Note]<br />需要 <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">功能層級</a> 10_0 或更新版本的硬體。</blockquote><br /> | 




 

</dd> <dt>

<span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*選擇*
</dt> <dd>

變數。 大括弧內的 case 語句會各自檢查此變數，以查看 SwitchValue 是否符合其特定 CaseValue。

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

一或多個 [語句](dx-graphics-hlsl-statement-blocks.md)。

</dd> </dl>

## <a name="remarks"></a>備註


```
[branch] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



相當於：


```
[branch] if( a == 2 )
    return 3;
else if( a == 1 )
    return 1;
else if( a == 0 )
    return 0;
else
    return 6;
```



以下是 forcecase 和呼叫流程式控制制屬性的範例使用方式：


```
[forcecase] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}

[call] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Urlmon.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Flow控制](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

