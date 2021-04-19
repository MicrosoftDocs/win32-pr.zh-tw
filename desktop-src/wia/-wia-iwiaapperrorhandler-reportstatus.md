---
description: 處理影像資料傳輸期間的裝置狀態和錯誤訊息，並向使用者顯示訊息。
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'IWiaAppErrorHandler：： ReportStatus 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971043"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a>IWiaAppErrorHandler：： ReportStatus 方法

處理影像資料傳輸期間的裝置狀態和錯誤訊息，並向使用者顯示訊息。

## <a name="syntax"></a>語法


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

未使用。 設定為0。

</dd> <dt>

*pWiaItem2* \[在\]
</dt> <dd>

類型： **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

要傳送之專案的指標。

</dd> <dt>

_hrStatus * \[ in\]
</dt> <dd>

類型： **HRESULT**

裝置狀態碼。

</dd> <dt>

*lPercentComplete* \[在\]
</dt> <dd>

類型： **LONG**

目前作業已完成的百分比。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果不可能從錯誤復原，則會傳回 *hrStatus* 。 否則，它會傳回下列其中一個值。



| 傳回碼                                                                                              | Description                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                     | 如果 *hrStatus* 是錯誤，則會採取適當的動作來更正錯誤，而且可以繼續傳送。 如果 *hrStatus* 是參考資訊，使用者就會收到非強制回應對話方塊的通知，並選擇不要取消傳送。<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                  | 使用者取消了從錯誤處理常式非強制回應對話方塊的傳送。 無論 *hrStatus* 為何，都可以在任何時間點傳回這個值。 <br/>                                                                                      |
| <dl> <dt>**\_ \_ 未處理 WIA \_ 狀態**</dt> </dl> | 未採取任何動作;亦即，不會對使用者顯示任何對話方塊。 將會叫用下一個錯誤處理常式。 錯誤處理常式的順序如下：應用程式、驅動程式和系統預設值。<br/>                                                 |



 

## <a name="remarks"></a>備註

*LPercentComplete* 參數可讓 [錯誤處理常式] 視窗顯示進度。 例如，驅動程式可能會提供「準備」所需時間的估計。 傳遞至 **IWiaAppErrorHandler：： ReportStatus** 的 *lPercentComplete* 參數，與驅動程式設定為 [**WiaTransferParams**](-wia-wiatransferparams.md)結構的 **lPercentComplete** 值相同。

錯誤處理常式可以使用成功和失敗的宏，以找出 *hrStatus* 的嚴重性 \_ 錯誤或嚴重性 \_ 是否成功。

如果 *hrStatus* 為嚴重性 \_ 成功，則應允許使用者取消傳輸。

如果 *hrStatus* 是嚴重性 \_ 錯誤，則錯誤處理常式應該會顯示應用程式父視窗所擁有的強制回應對話方塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



 

 




