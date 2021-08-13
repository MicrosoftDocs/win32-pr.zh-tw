---
description: WiaTransferParams 會在資料傳輸期間傳送至應用程式，Windows 影像取得 (WIA) 執行時間系統轉換為 IWiaTransferCallback：： TransferCallback 方法。
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: 'WiaTransferParams 結構 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 7d128a39ff5d9d29bf0766273adaace7eae86b10c9556284c1f5b6f1c9285d30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449901"
---
# <a name="wiatransferparams-structure"></a>WiaTransferParams 結構

**WiaTransferParams** 會在資料傳輸期間傳送至應用程式，Windows 影像取得 (WIA) 執行時間系統轉換為 [**IWiaTransferCallback：： TransferCallback**](-wia-iwiatransfercallback-transfercallback.md)方法。

## <a name="syntax"></a>語法


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a>成員

<dl> <dt>

**lMessage**
</dt> <dd>

類型： **LONG**

</dd> <dd>

表示資料傳輸的狀態。

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**WIA \_ 傳送 \_ 訊息 \_ 狀態**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**WIA \_ 傳送 \_ \_ 資料流程結尾 \_ \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**WIA \_ 傳送 \_ 訊息 \_ 結束 \_ \_ 傳送**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**WIA \_ 傳送 \_ MSG \_ 裝置 \_ 狀態**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**WIA \_ 傳送 \_ MSG 的 \_ 新 \_ 頁面**


</dt> <dd></dd> </dl> </dd> <dt>

**lPercentComplete**
</dt> <dd>

類型： **LONG**

</dd> <dd>

表示資料傳輸的進度（以百分比表示）。

</dd> <dt>

**ulTransferredBytes**
</dt> <dd>

類型： **ULONG64**

</dd> <dd>

指出傳送的資料量。

</dd> <dt>

**hrErrorStatus**
</dt> <dd>

類型： **HRESULT**

</dd> <dd>

驅動程式所設定之裝置的狀態或錯誤狀態;例如，「準備」。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl> |



 

 




