---
title: /target 參數
description: /Target 參數可讓 MIDL 編譯器只啟用最新版本 Windows 的優化功能。 /Target 參數會自動啟用額外的參數。
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- /target 參數 MIDL
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: b1c4292ed3b1fba2d3f3d9bd350c06cee89d2ba569103db1b677bc690be4af15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895778"
---
# <a name="target-switch"></a>/target 參數

**/Target** 參數可讓 MIDL 編譯器只啟用最新版本 Windows 的優化功能。 **/Target** 參數會自動啟用額外的參數。

``` syntax
midl /target level
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*level* 
</dt> <dd>

指定目標層級，例如 NT50、NT51、NT60、NT61、NT62 或 NT100。

</dd> </dl>

## <a name="remarks"></a>備註

**/Target** 參數會根據下表所指定的作業系統，自動啟用其他參數：



| 作業系統 | /target 層級 | 啟用的開關                     |
|------------------|---------------|----------------------------------------|
| Windows 2000     | NT50          | /Oicf/error all/robust               |
| Windows XP       | NT51          | /Oicf/error all/robust/protocol all |
| Windows Vista    | NT60          | /Oicf/error all/robust/protocol all |
| Windows 7        | NT61          | /Oicf/error all/robust/protocol all |
| Windows 8        | NT62          | /Oicf/error all/robust/protocol all |
| Windows 10       | NT100         | /Oicf/error all/robust/protocol all |
 

為了確保在 **/target** 參數所指定的系統上執行存根，MIDL 會在有較新版本的 Windows 的可用功能時發出錯誤。 下表指定啟用此功能所需的最小 **/target** 層級。 較高的目標層級包含來自較低目標層級的所有功能。



| 至少需要/target 層級 | 功能                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NT50                           | /robust<br/> \[message\]<br/> \[async\]<br/> \[非同步 \_ uuid\]<br/> \[\]在/Oicf 模式中通知<br/> \[\] \[ \] 在/Oicf 模式中進行編碼或解碼<br/>                   |
| NT51                           | /protocol 64 位支援<br/> \[部分 \_ 忽略\]<br/> \[強制 \_ 配置\]<br/>                                                                                                 |
| NT60                           | 強制複雜結構封送處理<br/> 陣列或結構中的內容控制碼<br/> \[\]可變大小字串的範圍支援<br/> \[輸入 \_ strict \_ 內容 \_ 控制碼\]<br/> |
| NT61                           | 具有小於32方法之介面的直接 COM stub 呼叫需要連結具有 **OLE32.DLL** 的 com 存根。<br/>                                                                          |
| NT62                           | ARM 支援<br/> WinRT 支援<br/>                                                                                                                                                   |
| NT100                          | \[system_handle \] 支援<br /> |


 

## <a name="examples"></a>範例

**midl/target NT50**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>
