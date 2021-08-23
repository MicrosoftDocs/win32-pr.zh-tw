---
description: '\_線路裝置的狀態變更時，會傳送 TAPI 線路 LINEDEVSTATE 訊息。 應用程式可以叫用 lineGetLineDevStatus，以判斷該行的新狀態。'
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: 'LINE_LINEDEVSTATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261e7527354b84801437e48ffc13ba4dbad60ced0cca61be65eb96ce6417bb10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682383"
---
# <a name="line_linedevstate-message"></a>行 \_ LINEDEVSTATE 訊息

線路裝置的狀態變更時，會傳送 TAPI **線路 \_ LINEDEVSTATE** 訊息。 應用程式可以叫用 [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) ，以判斷該行的新狀態。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

線路裝置的控制碼。 當 *dwParam1* 為 LINEDEVSTATE 重新初始化時，此參數為 **Null** \_ 。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟行時所提供的回呼實例。 如果 *dwParam1* 參數為 LINEDEVSTATE \_ 重新初始化，則 *dwCallbackInstance* 參數無效，並設定為零。

</dd> <dt>

*dwParam1* 
</dt> <dd>

已變更的行裝置狀態專案。 參數可以是一或多個 [**LINEDEVSTATE \_ 常數**](linedevstate--constants.md)。

</dd> <dt>

*dwParam2* 
</dt> <dd>

此參數的解讀取決於 *dwParam1* 的值。 如果 *dwParam1* 是 LINEDEVSTATE \_ 響鈴，則 *dwParam2* 會包含環形模式，而參數會使用它來指示線路響鈴。 有效的環形模式是在一到 **dwNumRingModes** 範圍內的數位，其中 **dwNumRingModes** 是行裝置功能。

如果 *dwParam1* 是 LINEDEVSTATE \_ 重新初始化，而且由於將新的 API 訊息轉譯為重新初始化訊息而導致 TAPI 發出訊息，則 *dwParam2* 會包含原始訊息的 *dwMsg* 參數 (例如， [**line \_ CREATE**](line-create.md) 或 line \_ LINEDEVSTATE) 。 如果 *dwParam2* 為零，這表示重新初始化訊息是 "REAL" 重新初始化訊息，要求應用程式以最早的便利性呼叫 [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) 。

</dd> <dt>

*dwParam3* 
</dt> <dd>

此參數的解讀取決於 *dwParam1* 的值。 如果 *dwParam1* 是 LINEDEVSTATE \_ 響鈴， *dwParam3* 就會包含此環形事件的響鈴計數。 響鈴計數從零開始。

如果 *dwParam1* 是 LINEDEVSTATE \_ 重新初始化，且訊息是由 TAPI 因為將新的 API 訊息轉譯為重新初始化訊息而發出，則 *dwParam3* 包含原始訊息的 *dwParam1* 參數 (例如，LINEDEVSTATE \_ TRANSLATECHANGE 或其他 LINEDEVSTATE \_ 值（如果 *dwParam2* 為 line \_ LINEDEVSTATE）或新的裝置識別碼（如果 *dwParam2* 是行 [**\_ 建立**](line-create.md)) ）。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

您可以使用 [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)來控制 **行 \_ LINEDEVSTATE** 訊息的傳送。 應用程式可以指出其想要收到通知的狀態專案變更。 預設會停用所有狀態報表，但 \_ 不能停用 LINEDEVSTATE 重新初始化。 這則訊息會傳送至具有該行控制碼的所有應用程式，包括呼叫 [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) 且 *dwPrivileges* 參數設定為 LINECALLPRIVILEGE \_ NONE、LINECALLPRIVILEGE \_ OWNER、LINECALLPRIVILEGE \_ MONITOR 或允許的組合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ 關閉**](line-close.md)
</dt> <dt>

[**行 \_ 建立**](line-create.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




