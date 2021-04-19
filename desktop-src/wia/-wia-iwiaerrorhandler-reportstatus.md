---
description: 處理影像資料傳輸期間的狀態和錯誤訊息，並將其顯示給使用者。
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'IWiaErrorHandler：： ReportStatus 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 30a082502d4c7bc5b789fd1ec19fdb76f63d8fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974284"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a>IWiaErrorHandler：： ReportStatus 方法

處理影像資料傳輸期間的狀態和錯誤訊息，並將其顯示給使用者。

## <a name="syntax"></a>語法


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* \[在\]
</dt> <dd>

類型： **HWND**

**HWND** ，也就是訊息視窗的父視窗。

</dd> <dt>

*punkItem* \[在\]
</dt> <dd>

類型： **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

要傳送之專案的 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。 此物件至少會執行 [_ *IWiaItem2* *](-wia-iwiaitem2.md)和 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)。

</dd> <dt>

*hrStatus* \[在\]
</dt> <dd>

類型： **HRESULT**

**HRESULT** ，這是 [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)所接收的狀態碼。

</dd> <dt>

*cbResLength* \[在\]
</dt> <dd>

類型： **LONG**

**LONG** 是 *>pbdata* 所參考的資料大小。

</dd> <dt>

*>pbdata* \[在\]
</dt> <dd>

類型： **BYTE \** _

[_ *BandedDataCallback* *](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)所接收之資料緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果無法從復原錯誤，則傳回 *hrStatus* 。 否則，它會傳回下列其中一個值。



| 傳回碼                                                                             | Description                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 已採取適當的動作來修正錯誤，而且可以繼續傳送。 <br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 未採取任何動作來處理使用者的錯誤或報告狀態。 <br/>                |
| <dl> <dt>**E \_ 中止**</dt> </dl> | 使用者選擇中止傳送以回應所顯示的對話方塊。 <br/>        |



 

## <a name="remarks"></a>備註

Windows 映像取得 (WIA) 2.0 會在驅動程式將 **IT \_ MSG \_ 裝置 \_ 狀態** 消息傳送至 [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)時呼叫 **IWiaErrorHandler：： ReportStatus** 。 這個方法會處理訊息，並向使用者顯示狀態或錯誤的相關資訊。 如果訊息是關於錯誤，則方法可讓使用者選擇（可能的話），是否嘗試從錯誤中復原並繼續傳送或中止。

*hrStatus* 設定為 WIA \_ 狀態 \_ 傳輸 \_ 開始，以通知處理常式已開始傳送。 當傳送完成時，它會設定為 WIA \_ 狀態 \_ 傳輸 \_ 結束。

如果 *hrStatus* 為嚴重性 \_ 成功，則應允許使用者取消傳輸。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



 

 
