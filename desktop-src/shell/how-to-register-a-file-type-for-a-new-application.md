---
description: 如果您打算將一或多個檔案類型與新的應用程式產生關聯，您必須為要與應用程式建立關聯的每個檔案類型定義 ProgID。
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: 如何註冊新應用程式的檔案類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de165d378d27c6891b681f95da7242b026844bd7734709ebd272c06edf40e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859658"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a>如何註冊新應用程式的檔案類型

如果您打算將一或多個檔案類型與新的應用程式產生關聯，您必須為要與應用程式建立關聯的每個檔案類型定義 ProgID。

若要為您的應用程式所處理的每個唯一檔案類型建立 ProgID，請使用下列步驟。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

請注意，某些檔案類型有多個指向相同 ProgID 的副檔名;例如：

-   **HKEY \_類別 \_ ROOT** \\ **App** (您的 ProgID) 
-   **HKEY \_類別 \_ ROOT** \\ **.jpg** = app.config (檔案類型對應) 
-   **HKEY \_類別 \_ ROOT** \\ **. jpeg** = app.config

### <a name="step-2"></a>步驟 2:

當您安裝和卸載程式時，請移除 ProgID 值。

### <a name="step-3"></a>步驟 3：

卸載時，將檔案類型對應保持不變。 這樣做的運作方式是因為檔案類型對應會儲存在 HKEY 類別根目錄中的每位使用者 \_ \_ \\ ，而且系統會識別缺少 ProgID 值的情況，並忽略它。 將檔案類型對應保持不變，可避免只有當值仍指向您的 ProgID 時，才需要具有只會移除檔案類型對應的條件式程式碼。 在其他應用程式可能已變更的情況下，請務必避免這種情況，因此無法輕易地移除值。

### <a name="step-4"></a>步驟 4：

執行下列其中一項動作，以指定每個檔案類型 ProgID 之檔案類型描述的唯一值：

-   將 ProgID 的預設值保留為空白，在此情況下，系統會使用副檔名檔案。
-   透過 FriendlyTypeName 提供當地語系化的值，並且與直接讀取登錄的舊應用程式相容，請務必提供 ProgID 的預設值做為檔案類型描述 (也就是使用英文資源) 中的 FriendlyTypeName 所參考的相同值。

## <a name="remarks"></a>備註

如果您打算將檔案與現有的應用程式建立關聯，請在登錄中找出應用程式 ProgID。 如需詳細資訊，請參閱 [檔案類型](fa-file-types.md)。

 

 



