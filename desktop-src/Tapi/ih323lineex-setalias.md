---
description: SetAlias 方法會為位址設定預設的 H. 323 別名。 此別名將用於 h.264 呼叫設定 exchange，讓另一方知道此合作物件的名稱。
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: 'IH323LineEx：： SetAlias 方法 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995925"
---
# <a name="ih323lineexsetalias-method"></a>IH323LineEx：： SetAlias 方法

\[**SetAlias** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**SetAlias** 方法會為位址設定預設的 H. 323 別名。 此別名將用於 h.264 呼叫設定 exchange，讓另一方知道此合作物件的名稱。

第二次呼叫這個方法將會覆寫前一個別名。

只有當 TSP 沒有其他方法可尋找適當的別名時，才會使用此介面上設定的別名。 未來，將閘道管理員支援新增至 TSP 時，註冊至閘道管理員或由閘道管理員指派的別名將會覆寫透過這個方法所設定的任何內容。

## <a name="syntax"></a>語法


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*strAlias* \[在\]
</dt> <dd>

要使用的別名（以 Unicode 為依據）。 不需要 **Null** 終止。

</dd> <dt>

*dwLength* \[在\]
</dt> <dd>

別名名稱的長度（以字元數為單位），包括 **null** 結束字元。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                               | Description                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 方法成功。<br/>                                                                                                     |
| <dl> <dt>**E \_ 指標**</dt> </dl> | *DwLength* 中指出的字元數超過 *strAlias* 參數中的實際字元數。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>H323priv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




