---
title: IMsTscAx VerticalScrollBarVisible 屬性
description: 指出控制項是否顯示垂直捲動條。
ms.assetid: b31e2db3-b367-4900-a2c6-51fd794341c2
ms.tgt_platform: multiple
keywords:
- VerticalScrollBarVisible 屬性遠端桌面服務
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，VerticalScrollBarVisible 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.VerticalScrollBarVisible
- IMsTscAx.get_VerticalScrollBarVisible
- IMsRdpClient.VerticalScrollBarVisible
- IMsRdpClient.get_VerticalScrollBarVisible
- IMsRdpClient2.VerticalScrollBarVisible
- IMsRdpClient2.get_VerticalScrollBarVisible
- IMsRdpClient3.VerticalScrollBarVisible
- IMsRdpClient3.get_VerticalScrollBarVisible
- IMsRdpClient4.VerticalScrollBarVisible
- IMsRdpClient4.get_VerticalScrollBarVisible
- IMsRdpClient5.VerticalScrollBarVisible
- IMsRdpClient5.get_VerticalScrollBarVisible
- IMsRdpClient6.VerticalScrollBarVisible
- IMsRdpClient6.get_VerticalScrollBarVisible
- IMsRdpClient7.VerticalScrollBarVisible
- IMsRdpClient7.get_VerticalScrollBarVisible
- IMsRdpClient8.VerticalScrollBarVisible
- IMsRdpClient8.get_VerticalScrollBarVisible
- IMsRdpClient9.VerticalScrollBarVisible
- IMsRdpClient9.get_VerticalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1365a0ab6d4a1411d78496cf157f3bc49fe5db15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464681"
---
# <a name="imstscaxverticalscrollbarvisible-property"></a>IMsTscAx：： VerticalScrollBarVisible 屬性

指出控制項是否顯示垂直捲動條。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_VerticalScrollBarVisible(
  [out] BOOL *pfVScrollVisible
);
```



## <a name="property-value"></a>屬性值

如果可以看到垂直捲動條，則此參數的值為 **TRUE** ，否則為 **FALSE** 。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

如果目前控制項的高度小於桌面的高度，控制項會自動顯示垂直捲動條。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





