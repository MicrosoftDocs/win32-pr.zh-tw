---
title: 'IMAPI.EXE 資料類型 (Imapi2) '
description: 光學媒體和相關聯裝置的規格會定義專案的範圍值，例如 DVD 結構描述、光碟資訊描述和功能頁面大小。
ms.assetid: 8797a8d0-5ce5-4b16-9d41-c22fa0d67dcf
keywords:
- ULONG_IMAPI2_DVD_STRUCTURE
- ULONG_IMAPI2_ADAPTER_DESCRIPTOR
- ULONG_IMAPI2_DEVICE_DESCRIPTOR
- ULONG_IMAPI2_DISC_INFORMATION
- ULONG_IMAPI2_TRACK_INFORMATION
- ULONG_IMAPI2_FEATURE_PAGE
- ULONG_IMAPI2_MODE_PAGE
- ULONG_IMAPI2_ALL_FEATURE_PAGES
- ULONG_IMAPI2_ALL_PROFILES
- ULONG_IMAPI2_ALL_MODE_PAGES
- ULONG_IMAPI2_NONZERO
- ULONG_IMAPI2_NOT_NEGATIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f003c2e03ff3d21623111d3d43a83cddf43e31c64557cfce18b5a401cdcd5d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612008"
---
# <a name="imapi-data-types"></a>IMAPI.EXE 資料類型

光學媒體和相關聯裝置的規格會定義專案的範圍值，例如 DVD 結構描述、光碟資訊描述和功能頁面大小。 IMAPI.EXE 會定義下列不帶正負號的長整數 (ULONG) 強制範圍值限制的類型。 這些類型會嚴格定義為參數的最佳 IDL 驗證，以及做為相關呼叫端的檔，以提供特定資料傳輸作業的上限。


```C++
typedef ULONG ULONG_IMAPI2_DVD_STRUCTURE;
typedef ULONG ULONG_IMAPI2_ADAPTER_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DEVICE_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DISC_INFORMATION;
typedef ULONG ULONG_IMAPI2_TRACK_INFORMATION;
typedef ULONG ULONG_IMAPI2_FEATURE_PAGE;
typedef ULONG ULONG_IMAPI2_MODE_PAGE;
typedef ULONG ULONG_IMAPI2_ALL_FEATURE_PAGES;
typedef ULONG ULONG_IMAPI2_ALL_PROFILES;
typedef ULONG ULONG_IMAPI2_ALL_MODE_PAGES;
typedef ULONG ULONG_IMAPI2_NONZERO;
typedef ULONG ULONG_IMAPI2_NOT_NEGATIVE;
```





| 資料類型                                                                                                                                  | 描述                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**ULONG \_ IMAPI2 \_ DVD \_ 結構**                | 範圍：0、65535 (0、0x0000FFFF) <br/> 因為有兩個位元組的配置欄位，所以 DVD 結構限制為64KB。<br/>                                                                                                                                                                                     |
| <span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**ULONG \_ IMAPI2 \_ 介面卡 \_ 描述項** | 範圍：0、268435455 (0、0x0FFFFFFF) <br/> 介面卡描述項的大小不會以隱含方式限制。<br/>                                                                                                                                                                                                |
| <span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**ULONG \_ IMAPI2 \_ 裝置 \_ 描述項**    | 範圍：0、268435455 (0、0x0FFFFFFF) <br/> 裝置描述項的大小不會以隱含方式限制。<br/>                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**ULONG \_ IMAPI2 \_ 光碟 \_ 資訊**       | 範圍：0、65538 (0、0x00010002) <br/> [大小] 欄位的光碟資訊限制為64KB 加2個位元組。<br/>                                                                                                                                                                                         |
| <span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**ULONG \_ IMAPI2 \_ 追蹤 \_ 資訊**    | 範圍：0、65538 (0、0x00010002) <br/> [大小] 欄位的追蹤資訊限制為64KB 加2個位元組。<br/>                                                                                                                                                                                        |
| <span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**ULONG \_ IMAPI2 \_ 功能 \_ 頁面**                   | 範圍： 0256 (0，0x00000100) <br/> 單一功能頁面的限制為256個位元組。<br/>                                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**ULONG \_ IMAPI2 \_ 模式 \_ 頁面**                            | 範圍： 0257 (0，0x00000101) <br/> 單一模式頁面的限制為257個位元組。<br/>                                                                                                                                                                                                                    |
| <span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**ULONG \_ IMAPI2 \_ 所有 \_ 功能 \_ 頁面**   | 範圍：0、65536 (0、0x00010000) <br/> 功能的數目限制為兩個位元組的欄位。<br/>                                                                                                                                                                                                       |
| <span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**ULONG \_ IMAPI2 \_ 所有 \_ 設定檔**                   | 範圍：0、63 (0、0x0000003F) <br/> 裝置的設定檔數目是適用于單一功能的設定檔數目。 每個設定檔都會佔用四個位元組。 單一功能可以保留252個額外的資料位元組，足以儲存最多63個設定檔。<br/>                                 |
| <span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**ULONG \_ IMAPI2 \_ 所有 \_ 模式 \_ 頁面**            | 範圍：0、32763 (0、0x00007FFB) <br/> 裝置的模式頁面計數。 計數（via 模式 \_ SENSE10）受限於雙位元組欄位。<br/> 模式參數標頭是8個位元組。 每個頁面至少都有兩個位元組。 模式頁面的最大數目是32763： (65535-8) /2 四捨五入。<br/> |
| <span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**ULONG \_ IMAPI2 \_ 非零**                                   | 範圍：1、2147483647 (1、0x7FFFFFFF) <br/> 泛型非零值，可用來驗證值不是零。<br/>                                                                                                                                                                              |
| <span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**ULONG \_ IMAPI2 \_ 非 \_ 負值**                   | 範圍：0、2147483647 (0、0x7FFFFFFF) <br/> 具有非負數值的32位整數。<br/>                                                                                                                                                                                                              |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Imapi2。h</dt> </dl> |



 

 





