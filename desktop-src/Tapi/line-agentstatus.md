---
description: '\_當應用程式目前已開啟的那一行上的 ACD 代理程式狀態變更時，就會傳送 TAPI 線路 AGENTSTATUS 訊息。 應用程式可以叫用 lineGetAgentStatus 來判斷代理程式目前的狀態。'
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: 'LINE_AGENTSTATUS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32335e59352b773f84e8a0725c6fd97de679670cbd237f87c3e629985feb43a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959868"
---
# <a name="line_agentstatus-message"></a>行 \_ AGENTSTATUS 訊息

當應用程式目前已開啟的那一行上的 ACD 代理程式狀態變更時，就會傳送 TAPI **線路 \_ AGENTSTATUS** 訊息。 應用程式可以叫用 [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) 來判斷代理程式目前的狀態。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

應用程式狀態已變更之線路裝置的應用程式控制碼。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟呼叫的行時所提供的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

代理程式狀態變更所在行的位址識別碼。 位址識別碼會永久與位址相關聯;識別碼在作業系統升級之間會維持不變。

</dd> <dt>

*dwParam2* 
</dt> <dd>

指定已變更的代理程式狀態;可以是 [**LINEAGENTSTATUS \_ 常數**](lineagentstatus--constants.md)的組合。

</dd> <dt>

*dwParam3* 
</dt> <dd>

如果 *dwParam2* 包含 LINEAGENTSTATUS \_ 狀態位，則 *dwParam3* 會在 [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)中指出 **dwState** 成員的新值。 否則，此參數會設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

**LINE \_ AGENTSTATUS** 訊息不會傳送至支援舊版 TAPI 的應用程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




