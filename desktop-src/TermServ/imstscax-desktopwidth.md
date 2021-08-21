---
title: IMsTscAx DesktopWidth 屬性
description: 以圖元為單位，指定初始遠端桌面上的目前控制項寬度（以圖元為單位）。
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- DesktopWidth 屬性遠端桌面服務
- DesktopWidth 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，DesktopWidth 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca982303208bb2badecf210c9590f627a7b3b57c5acd9ecd7f8fee0bbb70ec93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058839"
---
# <a name="imstscaxdesktopwidth-property"></a>IMsTscAx：:D esktopWidth 屬性

以圖元為單位，指定初始遠端桌面上的目前控制項寬度（以圖元為單位）。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a>屬性值

新的寬度（以圖元為單位）。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

設定 **DesktopWidth** 屬性是選擇性的，但必須先設定，才能呼叫 [**連線**](imstscax-connect.md)方法。 如果未指定桌面寬度，或設定為零，則會將桌面寬度設定為控制項的寬度。 最小值和最大值取決於遠端桌面用戶端的作業系統版本。

<dl> <dt>

<span id="_"></span>Windows 8/Windows Server 2012
</dt> <dd>

200最小值8192，最大值

</dd> <dt>

<span id="_"></span>Windows 7/Windows Server 2008
</dt> <dd>

200最小值2048，最大值

</dd> <dt>

Windows Vista
</dt> <dd>

200最小值1200，最大值

</dd> </dl>

建立連線之後，控制項寬度的任何變更都不會變更遠端桌面的寬度。 相反地，控制項會在適當的情況下，顯示捲軸或將遠端桌面置中。 若要變更使用中連接的桌面大小，請使用 [**IMsRdpClient8：： Reconnect**](imsrdpclient8-reconnect.md) 方法。

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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





