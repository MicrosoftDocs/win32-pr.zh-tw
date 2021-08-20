---
title: IMsRdpClientNonScriptable5 GetRemoteMonitorsBoundingBox 屬性
description: 指定遠端監視的周框。
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- GetRemoteMonitorsBoundingBox 屬性遠端桌面服務
- GetRemoteMonitorsBoundingBox 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，GetRemoteMonitorsBoundingBox 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b308bf95389dcf043e87565be365ec69ecc34500ac187ee11a679349f18ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129886"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a>IMsRdpClientNonScriptable5：： GetRemoteMonitorsBoundingBox 屬性

指定遠端監視的周框。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a>屬性值

接收矩形的左邊緣。

接收矩形的上邊緣。

接收矩形的右邊緣。

接收矩形的下邊緣。

## <a name="remarks"></a>備註

所有座標都是虛擬螢幕座標，相對於主要監視器的左上角。 如果這不是主要監視器，則部分或全部的值可能是負數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                             |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 定義為 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





