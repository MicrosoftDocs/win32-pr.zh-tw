---
title: IMsRdpDeviceCollection2 RedirectNow 方法
description: 強制將從集合中選取或取消選取的裝置重新導向或移除。
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- RedirectNow 方法遠端桌面服務
- RedirectNow 方法遠端桌面服務，IMsRdpDeviceCollection2 介面
- IMsRdpDeviceCollection2 介面遠端桌面服務，RedirectNow 方法
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60c92eff142305e95a71c69cdce9789b0d2316e3d5e60b703a7c1aa8e835688f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058916"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a>IMsRdpDeviceCollection2：： RedirectNow 方法

強制將從集合中選取或取消選取的裝置重新導向或移除。

## <a name="syntax"></a>語法


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* \[在\]
</dt> <dd>

類型： **[ **RedirectDeviceType**](redirectdevicetype.md)**

[**RedirectDeviceType**](redirectdevicetype.md)列舉的值，指定要重新導向的裝置類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RedirectDeviceType**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





