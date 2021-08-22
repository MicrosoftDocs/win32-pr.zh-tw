---
description: '\_當應用程式目前已開啟的那一行上的 ACD 代理程式狀態變更時，就會傳送 TAPI 線路 AGENTSPECIFIC 訊息。 應用程式可以叫用 lineGetAgentStatus 來判斷代理程式目前的狀態。'
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: 'LINE_AGENTSPECIFIC 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87b0e6f5c6c96842f70ebe46c0b72e33e6767c996fa2cc5b4d8e95ff0f08cd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867158"
---
# <a name="line_agentspecific-message"></a>行 \_ AGENTSPECIFIC 訊息

當應用程式目前已開啟的那一行上的 ACD 代理程式狀態變更時，就會傳送 TAPI **線路 \_ AGENTSPECIFIC** 訊息。 應用程式可以叫用 [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) 來判斷代理程式目前的狀態。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

應用程式線路裝置的控制碼。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟呼叫的行時所提供的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

與訊息相關聯之處理常式延伸模組的 [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) 結構中，處理常式延伸模組識別碼陣列的索引。

</dd> <dt>

*dwParam2* 
</dt> <dd>

特定于處理常式延伸模組。 一般來說，這個值是用來讓應用程式叫用 [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) 函式，以提取有關訊息的進一步詳細資料。

</dd> <dt>

*dwParam3* 
</dt> <dd>

特定于處理常式延伸模組。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

**LINE \_ AGENTSPECIFIC** 訊息不會傳送至支援舊版 TAPI 的應用程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




