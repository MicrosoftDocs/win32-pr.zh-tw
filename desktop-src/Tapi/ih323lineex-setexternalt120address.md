---
description: 應用程式會呼叫 SetExternalT120Address 方法來設定資料交換的外部 T. 120 位址。
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'IH323LineEx：： SetExternalT120Address 方法 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8889887c396c427c28ac2906206b3e3cbbcb102daa937720b6b879472b47bbdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992088"
---
# <a name="ih323lineexsetexternalt120address-method"></a>IH323LineEx：： SetExternalT120Address 方法

\[**SetExternalT120Address** 無法在 Windows Vista、Windows Server 2008 及後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

應用程式會呼叫 **SetExternalT120Address** 方法來設定資料交換的外部 T. 120 位址。 在 h.264 協商期間將會公告 T. 120 功能，而位址將用於 open 邏輯通道通知，讓另一個端點可以設定與接聽該位址的服務有關的 T. 120 個會話。 如果未呼叫此函式，則 h. 服務提供者將不會公告 T. 120 功能。

## <a name="syntax"></a>語法


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fEnable* \[在\]
</dt> <dd>

**TRUE** 表示啟用 T. 120 功能; **FALSE** 表示停用 T. 120 功能。

</dd> <dt>

*dwIP* \[在\]
</dt> <dd>

**DWORD** ，包含以外部的 T. 120 服務之主機位元組順序的 IP 位址。

</dd> <dt>

*wPort* \[在\]
</dt> <dd>

包含外部 T. 120 服務之埠的 **單字**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                          | 描述                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 方法成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>H323priv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




