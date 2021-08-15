---
title: 'DRM_LICENSE_STATE_DATA 結構 (Drmexternals .h) '
description: DRM \_ 授權 \_ 狀態 \_ 資料結構包含有關指定之 DRM 許可權的授權資訊。
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- DRM_LICENSE_STATE_DATA 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6703481dc1d3608a8bf08ab2bbd216db4a9ecdc91bd4604d2b9de7d7de4fa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848531"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a>DRM_LICENSE_STATE_DATA 結構 (Drmexternals .h) 

**Drm \_ 授權 \_ 狀態 \_ 資料** 結構包含有關指定之 [*DRM*](wmformat-glossary.md)許可權的 [*授權*](wmformat-glossary.md)資訊。

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

要顯示的字串類別。 如需可能的值及其意義，請參閱 [**DRM \_ 授權 \_ 狀態 \_ 類別目錄**](drm-license-state-category.md) 。

</dd> <dt>

**dwNumCounts**
</dt> <dd>

**DwCount** 中提供的專案數。 此值通常是0或1。

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

0或1或更多 **DWORD** 的陣列，代表在 **dwCategory** 中指定的動作可能執行的次數。 請參閱＜備註＞。

</dd> <dt>

**dwNumDates**
</dt> <dd>

**Datetime** 中提供的專案數。 通常不會使用兩個以上的日期，例如，具有從一個日期起生效的授權，直到另一個日期為止。

</dd> <dt>

**日期時間 \[ 4\]**
</dt> <dd>

一或多個 FILETIME 結構的陣列，代表授權中的一或多個日期。 特定日期的意義取決於 **dwCategory** 的值。

</dd> <dt>

**dwVague**
</dt> <dd>

下列的零或多個旗標與位 **or** 結合：



| 旗標                                    | 描述                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| DRM \_ 授權 \_ 狀態 \_ 資料 \_ 模糊        | 如果設定，則可能會有更多適用于內容的授權。                                                                                         |
| DRM \_ 授權 \_ 狀態 \_ 資料 \_ OPL \_ 存在 | 如果設定，授權就會包含輸出保護層級 (OPLs) 必須針對應用程式輸出的目的地進行抓取和檢查。 |
| \_提供 SAP 的 DRM 授權 \_ 狀態 \_ 資料 \_ \_ | 如果設定，則必須使用 (SAP) 的安全音訊路徑來傳遞內容。                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a>備註

當您指定其中一個 DRM 授權狀態屬性時，會從 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)的呼叫，將此結構傳回 (封裝于 [**WM \_ 授權 \_ 狀態 \_ 資料**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))結構) 。 這些屬性是：

-   [**DRM \_ LicenseState \_ 播放**](drm-licensestate-playback.md)
-   [**DRM \_ LicenseState \_ CopyToCD**](drm-licensestate-copytocd.md)
-   [**DRM \_ LicenseState \_ CopyToSDMIDevice**](drm-licensestate-copytosdmidevice.md)
-   [**DRM \_ LicenseState \_ CopyToNonSDMIDevice**](drm-licensestate-copytononsdmidevice.md)
-   [**DRM \_ LicenseState \_ CollaborativePlay**](drm-licensestate-collaborativeplay.md)
-   [**DRM \_ LicenseState \_ 複製**](drm-licensestate-copy.md)
-   [**DRM \_ LicenseState \_ PlaylistBurn**](drm-licensestate-playlistburn.md)

如果 **dwCategory** 是 **\_ 從 UNTIL 起算的 WM DRM \_ 授權 \_ 狀態 \_ 計數 \_ \_ ，** 則 **日期時間** 陣列通常會包含兩個日期： "FROM" 日期和 "UNTIL" 日期。 也可以指定兩個日期組來建立更複雜的授權。

**DwCount** 陣列的元素會對應至 **datetime** 陣列中所指定的日期或日期範圍。 如果 **dwCategory** 是 **從到 datetime 的 WM \_ DRM \_ 授權 \_ 狀態 \_ 計數 \_ \_** ，且 **datetime** 包含一對日期，則 **dwCount** 將會包含一個專案。 如果日期 **時間** 包含兩個日期組 (四個元素) ，則 **dwCount** 應該包含兩個元素，每個日期組各一個專案。

在某些情況下，使用者可能會被發給一個以上的檔案授權。 例如，他們可能已取得允許五個播放的授權，直到當月結束為止，並于稍後取得無限制許可權的第二個授權。 在這種情況下，DRM \_ 授權 \_ 狀態 \_ 資料 \_ 模糊旗標會設定在 **dwVague** () 中， `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` 而 drm 元件會使用演算法來判斷最可能套用的許可權集合。 當某個授權到期時，DRM 元件將會檢查剩餘的授權 (s) ，依此類推，直到所有授權都過期為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                      |
| 版本<br/>                  | WindowsMedia Format 7 SDK 或更新版本的 SDK<br/>                       |
| 標頭<br/>                   | <dl> <dt>Drmexternals。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](structures.md)
</dt> </dl>

 

