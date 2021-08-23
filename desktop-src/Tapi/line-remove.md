---
description: '\_系統會傳送 TAPI 行移除訊息，通知應用程式移除 (從線路裝置的系統) 刪除。'
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: 'LINE_REMOVE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f13f36123cb8cb77bd2d4b78c3e69a2da1c027aef4dad1fc9dfd7f3c6a00399
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335918"
---
# <a name="line_remove-message"></a>行 \_ 移除訊息

系統會傳送 TAPI **行 \_ 移除** 訊息，通知應用程式移除 (從線路裝置的系統) 刪除。 一般而言，這不會用於暫時移除（例如，將 PCMCIA 裝置解壓縮），但僅適用于永久移除，如果重新初始化 TAPI，服務提供者將不會再回報該裝置。


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

已移除之行裝置的識別碼。

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

支援 TAPI 2.0 版或更新版本的應用程式會傳送 **一行 \_ 移除** 訊息。 這會通知他們裝置已從系統中移除。 如果應用程式已開啟行，則在每個行控制碼上的行 **\_ 移除** 訊息前面會有 [**一行 \_ 關閉**](line-close.md) 訊息。 此訊息會傳送至所有支援 TAPI 2.0 版或更新版本的應用程式，這些應用程式已呼叫 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)，包括當時沒有任何線路裝置開啟的應用程式。

較舊的應用程式會傳送 [**一行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息 \_ ，指定 LINEDEVSTATE 已移除，後面接著行 \_ 關閉訊息。 但是，這些較舊的應用程式不像 **行 \_ 移除** 訊息，只有在移除時有行開啟時，才可以接收這些訊息。 如果它們沒有開啟的行，表示裝置已移除的唯一指示將會 \_ 在嘗試存取裝置時收到 LINEERR 的 NODEVICE 錯誤。

移除裝置之後，依裝置識別碼存取裝置的任何嘗試都會導致 LINEERR \_ NODEVICE 錯誤。 在所有 TAPI 應用程式都關機之後，重新開機 tapi 之後，當 TAPI 重新初始化時，移除的裝置就不再佔用裝置識別碼。

> [!Note]  
> 執行：此為 TAPI 會傳回這個 LINEERR \_ NODEVICE; 從服務提供者收到 **行 \_ 移除** 訊息之後，就不會使用該線路裝置識別碼對該服務提供者進行進一步的呼叫。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ 關閉**](line-close.md)
</dt> <dt>

[**行 \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




