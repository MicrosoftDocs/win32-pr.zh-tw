---
title: 'DRM_LICENSE_STATE_DATA 結構 (Wmdrmsdk .h) '
description: DRM \_ 授權 \_ 狀態 \_ 資料結構包含 drm 許可權的授許可權制相關資訊。
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- DRM_LICENSE_STATE_DATA 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ba00384ec7c3340aa099f1b427cd8953969704bd0585f0da58cd4fd0ffd6ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708928"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a>DRM_LICENSE_STATE_DATA 結構 (Wmdrmsdk .h) 

**Drm \_ 授權 \_ 狀態 \_ 資料** 結構包含 drm 許可權的授許可權制相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**dwStreamId**
</dt> <dd>

要套用授權的串流號碼。 必須是0，表示授權會套用至檔案中的所有資料流程。

</dd> <dt>

**dwCategory**
</dt> <dd>

要顯示的字串類別。 如需可能的值及其意義，請參閱 [**DRM \_ 授權 \_ 狀態 \_ 類別目錄**](drmdrm-license-state-category.md) 。

</dd> <dt>

**dwNumCounts**
</dt> <dd>

**DwCount** 中提供的專案數。 此值通常是0或1。

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

0或1或更多 **DWORD** 值的陣列，代表可執行 **dwCategory** 中指定之動作的次數。 請參閱＜備註＞。

</dd> <dt>

**dwNumDates**
</dt> <dd>

**Datetime** 中提供的專案數。 通常不會使用兩個以上的日期，例如，具有從一個日期起生效的授權，直到另一個日期為止。

</dd> <dt>

**日期時間 \[ 4\]**
</dt> <dd>

一或多個 **FILETIME** 結構的陣列，代表授權中的一或多個日期。 特定日期的意義取決於 **dwCategory** 的值。

</dd> <dt>

**dwVague**
</dt> <dd>

下列的零或多個旗標與位 **or** 結合：



| 旗標                                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DRM \_ 授權 \_ 狀態 \_ 資料 \_ 模糊        | 如果設定，則可能會有更多適用于內容的授權。 要確定適用于指定金鑰識別碼之個別授權的唯一方法是列舉授權。 若要這樣做，請呼叫 [**IWMDRMLicenseManagement：： CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)，並傳遞金鑰識別碼作為 bstrKID 參數。 然後使用已取出的 IWMDRMLicense 介面來檢查授權。 |
| DRM \_ 授權 \_ 狀態 \_ 資料 \_ OPL \_ 存在 | 如果設定，授權就會包含輸出保護層級 (OPLs) 必須針對應用程式輸出的目的地進行抓取和檢查。                                                                                                                                                                                                                                                                                  |
| \_提供 SAP 的 DRM 授權 \_ 狀態 \_ 資料 \_ \_ | 如果設定，則必須使用 (SAP) 的安全音訊路徑來傳遞內容。                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a>備註

藉由呼叫 **IWMDRMLicenseQuery：： QueryLicenseState**，即可取出此結構。

如果 **dwCategory** 是 **\_ \_ \_ \_ \_ 從 \_ UNTIL 起算的 WM DRM 授權狀態計數**，則 **日期時間** 陣列通常會包含兩個日期： "FROM" 日期和 "UNTIL" 日期。 也可以指定兩個日期組來建立更複雜的授權。

**DwCount** 陣列的元素會對應至 **datetime** 陣列中所指定的日期或日期範圍。 如果 **dwCategory** 是 **從到 datetime 的 WM \_ DRM \_ 授權 \_ 狀態 \_ 計數 \_ \_** ，且 **datetime** 包含一對日期，則 **dwCount** 將會包含一個專案。 如果日期 **時間** 包含兩個日期組 (四個元素) ，則 **dwCount** 應該包含兩個元素，每個日期組各一個專案。

在某些情況下，使用者可能會被發給一個以上的檔案授權。 例如，他們可能已取得允許五個播放的授權，直到當月結束為止，並于稍後取得無限制許可權的第二個授權。 在這種情況下，DRM \_ 授權 \_ 狀態 \_ 資料 \_ 模糊旗標會設定在 **dwVague** () 中， `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` 而 drm 元件會使用演算法來判斷最可能套用的許可權集合。 當某個授權到期時，DRM 元件將會檢查剩餘的授權，依此類推，直到所有授權都過期為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





