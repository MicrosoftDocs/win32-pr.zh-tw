---
title: IMsRdpClient8 Reconnect 方法
description: 重新連接到具有新桌面寬度和高度的遠端會話。
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Reconnect 方法遠端桌面服務
- Reconnect 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務、Reconnect 方法
- Reconnect 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務、Reconnect 方法
- Reconnect 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務、Reconnect 方法
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509474"
---
# <a name="imsrdpclient8reconnect-method"></a>IMsRdpClient8：： Reconnect 方法

重新連接到具有新桌面寬度和高度的遠端會話。 控制項必須已連接到遠端會話，這個方法才能成功。

## <a name="syntax"></a>語法


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulWidth* \[在\]
</dt> <dd>

類型： **ULONG**

新的桌面寬度（以圖元為單位）。 如需值限制，請參閱 [**DesktopWidth**](imstscax-desktopwidth.md) 屬性。

</dd> <dt>

*ulHeight* \[在\]
</dt> <dd>

類型： **ULONG**

新的桌面高度（以圖元為單位）。 如需值限制，請參閱 [**DesktopHeight**](imstscax-desktopheight.md) 屬性。

</dd> <dt>

*pReconnectStatus* \[退出，retval\]
</dt> <dd>

類型： **[**ControlReconnectStatus**](controlreconnectstatus.md) \** _

[_ *ControlReconnectStatus* *](controlreconnectstatus.md)變數的指標，此變數會接收重新連接作業的狀態。

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
| IID<br/>                      | IID \_ IMsRdpClient8 定義為4247E044-9271-43A9-BC49-E2AD9E855D62<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**ControlReconnectStatus**](controlreconnectstatus.md)
</dt> </dl>

 

 





