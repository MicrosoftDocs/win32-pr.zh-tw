---
description: CPersistStream 是篩選的持續性屬性基類 (也就是，在儲存的圖形) 中篩選屬性。
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: CPersistStream 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream
api_type:
- COM
api_location: ''
ms.openlocfilehash: 60a48b35ae1559e9b8dfa718c5bca38689cdf0101ce4a343a907b713c8988de0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073575"
---
# <a name="cpersiststream-class"></a>CPersistStream 類別

![cpersiststream 類別階層](images/pstrm01.png)

`CPersistStream` 是篩選的持續性屬性的基類 (也就是，在儲存的圖形) 中篩選屬性。

最簡單的使用方式 `CPersistStream` 是：

1.  排列篩選準則，以繼承這個類別。
2.  在您的類別中執行 [**WriteToStream**](cpersiststream-writetostream.md) 和 [**ReadFromStream**](cpersiststream-readfromstream.md) 。 這些函式會覆寫此處的函式，而不執行任何動作，而是做為預留位置。
3.  變更您的 **NonDelegatingQueryInterface** 以處理 **IPersistStream**。
4.  執行 [**SizeMax**](cpersiststream-sizemax.md) ，以傳回您儲存的資料位元組數上限。

    如果您儲存 Unicode™資料，請記住 WCHAR 是2個位元組。

5.  當您的資料變更時，請呼叫 [**SetDirty**](cpersiststream-setdirty.md)。

## <a name="version-numbers"></a>版本號碼

在某個時間點，您可能會決定改變或擴充資料的格式。 然後，您會希望所有舊儲存的串流中都有一個版本號碼，如此您就可以在讀取它們時告訴您，是否代表舊的或新的表單。 為了協助您，這個類別會寫入和讀取版本號碼。 寫入時，它會呼叫 [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) 來查詢目前正在使用的軟體版本。  (實際上是檔案中資料配置的版本號碼。 ) 它會將此資料寫入資料中的第一件事。 如果您想要變更版本，請執行 (覆寫) **GetSoftwareVersion**。 它會先將檔案中的版本號碼 **讀入 \_ mp dwFileVersion** ，然後再呼叫 [**ReadFromStream**](cpersiststream-readfromstream.md)，因此在 **ReadFromStream** 中，您可以檢查 **mp \_ dwFileVersion** 以查看是否正在讀取舊的版本檔案。 通常，您應該接受版本比讀取的軟體版本還新的檔案。

**CPersistStream** 會實施 [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)。 如需更多的執行資訊，請參閱 Microsoft Platform SDK 中的 COM 參考。



| 受保護的資料成員                                          | 描述                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| Mp \_ dwFileVersion                                              | 檔案的版本號碼。                                                   |
| Mp \_ fDirty                                                     | 必須儲存此資料流程的資料。                                           |
| 成員函數                                                | 描述                                                                   |
| [**CPersistStream**](cpersiststream-cpersiststream.md)         | 結構 **CPersistStream** 物件。                                       |
| [**SetDirty**](cpersiststream-setdirty.md)                     | 表示必須將物件儲存至資料流程。                        |
| 可覆寫的成員函式                                    | 描述                                                                   |
| [**GetClassID**](cpersiststream-getclassid.md)                 | 捕獲此資料流程的類別識別碼。                                |
| [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) | 抓取此檔案格式的版本號碼。                            |
| [**ReadFromStream**](cpersiststream-readfromstream.md)         | 從資料流程讀取篩選的資料。                                      |
| [**SizeMax**](cpersiststream-sizemax.md)                       | 抓取資料 (不包括) 的版本號碼所需的位元組數目。 |
| [**WriteToStream**](cpersiststream-writetostream.md)           | 將篩選的資料寫入至資料流程。                                       |
| IPersistStream 方法                                          | 描述                                                                   |
| [**GetSizeMax**](cpersiststream-getsizemax.md)                 | 抓取資料 (所需的位元組數目，包括) 的版本號碼。     |
| [**IsDirty**](cpersiststream-isdirty.md)                       | 檢查是否必須儲存物件。                                           |
| [**載入**](cpersiststream-load.md)                             | 將資料流程中的資料載入記憶體。                                   |
| [**儲存**](cpersiststream-save.md)                             | 將記憶體中的資料儲存至資料流程。                                     |



 

 

 
