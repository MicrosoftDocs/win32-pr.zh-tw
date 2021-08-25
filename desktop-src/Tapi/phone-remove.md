---
description: '\_系統會傳送 TAPI 電話移除訊息，以通知移除從電話裝置的系統) 移除 (刪除。'
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: 'PHONE_REMOVE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26be60c55b16d0126d0b3be107a95af17dd490c9329343bb27ac6496403d46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773898"
---
# <a name="phone_remove-message"></a>手機 \_ 移除訊息

系統會傳送 TAPI **電話 \_ 移除** 訊息，以通知移除從電話裝置的系統) 移除 (刪除。 一般而言，這不會用於暫時移除（例如，將 PCMCIA 裝置解壓縮），但僅適用于永久移除，如果重新初始化 TAPI，服務提供者將不會再回報該裝置。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

保留的。 設定為零。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

保留的。 設定為零。

</dd> <dt>

*dwParam1* 
</dt> <dd>

已移除之手機裝置的識別碼。

</dd> <dt>

*dwParam2* 
</dt> <dd>

保留的。 設定為零。

</dd> <dt>

*dwParam3* 
</dt> <dd>

保留的。 設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

應用程式 TAPI 2.0 版或更新版本會傳送 **電話 \_ 移除** 訊息。 這會通知他們裝置已從系統中移除。 如果應用程式已開啟電話，則 **電話 \_ 移除** 訊息前面會有每個電話控制碼上的 [**電話 \_ 關閉**](phone-close.md) 訊息。 這則訊息會傳送至所有支援 TAPI 2.0 版或更新版本的應用程式，這些應用程式已呼叫 [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)，包括當時未開啟任何手機裝置的應用程式。

繼承應用程式 (協商 TAPI 1.4 或更早版本的) 會傳送 [**電話 \_ 狀態**](phone-state.md) 消息，指出 PHONESTATE \_ 已移除，後面接著 [**電話 \_ 關閉**](phone-close.md) 訊息。 不過，不同于 **行動電話 \_ 的** 訊息，這些較舊的應用程式只有在移除手機時，才會收到這些訊息。 如果他們沒有開啟電話，則只有在裝置 \_ 嘗試存取裝置時，才會收到 PHONEERR NODEVICE 的指示。

移除裝置之後，依裝置識別碼存取裝置的任何嘗試都會導致 PHONEERR \_ NODEVICE 錯誤。 在所有 TAPI 應用程式都關機之後，重新開機 tapi 之後，當 TAPI 重新初始化時，移除的裝置就不再佔用裝置識別碼。

> [!Note]  
> 執行：它是 \_ 從服務提供者收到電話移除訊息之後，會傳回此 PHONEERR NODEVICE 訊息的 TAPI \_ ; 不會使用該電話裝置識別碼對該服務提供者進行其他呼叫。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**電話 \_ 關閉**](phone-close.md)
</dt> <dt>

[**電話 \_ 狀態**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




