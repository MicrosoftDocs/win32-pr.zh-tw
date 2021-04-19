---
description: 設定預設功能的喜好設定。
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'IH323LineEx：： SetDefaultCapabilityPreferrence 方法 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5604348eb80a3f423f6902f0a9a6e57204280c83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994220"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a>IH323LineEx：： SetDefaultCapabilityPreferrence 方法

\[**SetDefaultCapabilityPreferrence** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**SetDefaultCapabilityPreferrence** 方法會設定預設功能的喜好設定。 功能的預設權數為100。 如果應用程式為功能指定較高的權數，則在 h.264 協商期間會有較高的優先順序。 如果應用程式將功能的權數設定為0，它就不會用於 h. 協商。

這個方法是累計的。 例如，如果第一次呼叫此方法來停用功能，並再次呼叫以停用另一項功能，則這兩個功能會因為這兩個呼叫的結果而停用。

## <a name="syntax"></a>語法


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwNumCaps* \[在\]
</dt> <dd>

**DWORD** 值，包含使用此方法設定的功能數目。

</dd> <dt>

*pCapabilities* \[在\]
</dt> <dd>

功能陣列。 陣列的每個元素都是 [**H245 \_ 功能**](h245-capability.md) 值。

</dd> <dt>

*pWeights* \[在\]
</dt> <dd>

與功能相關聯的加權陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                                                                                                                                                                                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PCapabilities* 參數為 **Null**，或 *pWeights* 參數為 **null**，或 *pCapabilities* 和 *PWeights* 都是 **null**，或 pCapabilities 陣列包含不正確 h. 功能物件。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 無法讀取 *pWeights* 陣列的元素或 *pCapabilities* 陣列的元素。<br/>                                                                                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>H323priv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




