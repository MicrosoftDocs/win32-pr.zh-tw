---
title: 註冊
description: 註冊
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- 註冊 HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b378cd97bc9779951d62873d393009c98d32823
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375376"
---
# <a name="register"></a>註冊

選擇性的關鍵字，可將著色器變數指派給特定的暫存器，它會使用下列語法：



| ：註冊 ( *\[ 著色 \_ 器 \] 設定檔*， *輸入 \# \[ 子元件 \]* )  |
|----------------------------------------------------------------|



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="register"></span><span id="REGISTER"></span>註冊
</dt> <dd>

必要關鍵字。

</dd> <dt>

<span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[著色器 \_ 設定檔\]*
</dt> <dd>

選擇性 [著色器設定檔](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)，可以是著色器的目標，或只是 **ps** 或 **vs**。

</dd> <dt>

<span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*類型 \# \[ 子元件\]*
</dt> <dd>

註冊類型、數位和子元件宣告。

-   類型是下列其中一項：

    

    | 類型 | 註冊描述       |
    |------|----------------------------|
    | b    | 常數緩衝區            |
    | t    | 材質和材質緩衝區 |
    | c    | 緩衝區位移              |
    | s    | 取樣器                    |
    | u    | 未排序的存取權視圖      |

    

     

-   *\#* 這是暫存器編號，也就是整數。
-   *子元件* 是選擇性的整數數位。

</dd> </dl>

## <a name="remarks"></a>備註

您可以將一或多個註冊指派新增至相同的變數宣告，並以空格分隔。

針對全域範圍中的 Direct3D 10 變數， **register** 關鍵字的作用與 [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) 關鍵字相同。

## <a name="examples"></a>範例

以下是一些範例：


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[語法變數](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[ (DirectX HLSL) 的變數 ](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 