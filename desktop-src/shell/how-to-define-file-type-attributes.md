---
description: 在登錄中定義檔案類型屬性。
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: 如何定義檔案類型屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0a89f5770b55521ccdf51859bdde69ed58d05f864385e46f1d76e482319c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223572"
---
# <a name="how-to-define-file-type-attributes"></a>如何定義檔案類型屬性

將檔案類型屬性指派給相關聯的 ProgID，可讓您控制檔案類型行為的某些層面。 在 Windows Vista 之前，這些屬性可讓您限制使用者可以使用 [**資料夾選項**] 屬性索引標籤的範圍，以修改檔案類型的各個層面，例如其圖示或動詞。

檔案類型屬性是二進位旗標，會在檔案類型相關聯的 ProgID 子機碼中指定為 **reg \_ DWORD** 或 **reg \_ 二進位** 值。

若要指派檔案類型的屬性，請遵循下列步驟。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

將 EditFlags 專案新增至檔案類型的相關 ProgID 子機碼。

### <a name="step-2"></a>步驟 2:

將專案設定為適當的屬性值。

下列範例顯示 FTA \_ NoRemove (0x00000010) 和 FTA \_ NoNewVerb (0x00000020) 屬性為 myp 檔案類型設定的屬性。

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a>備註

旗標可以與邏輯 OR 結合，以形成單一屬性值。

如需可能的檔案類型屬性和其十六進位值的清單，以及以程式設計方式取得和設定這些值的詳細資訊，請參閱 [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags)。

 

 



