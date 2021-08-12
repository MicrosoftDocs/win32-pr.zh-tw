---
title: 將 ADSI Visual Basic 程式碼對應至 c + + 程式碼
description: ADSI 包含50以上的介面。
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a924f403dcbdbe89b1b0bbf846c95223b401a04d1925ce9362a5300faf828fe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179205"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a>將 ADSI Visual Basic 程式碼對應至 c + + 程式碼

ADSI 包含50以上的介面。 大部分的目錄作業只能使用五個介面完成。 這些包括：

-   [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

下表列出從 ADSI VB/VBS 程式碼到 c + + 程式碼的對應。 請注意，這不是完整的清單。



| VBS 程式碼                           | VC 程式碼                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| Set obj = GetObject ()               | hr = AdsGetObject ()                                                    |
| Obj。Put obj。取得 obj。父母         | IADs 或 IDirectoryObject                                              |
| Obj。建立 obj。刪除 obj。MoveHere | IADsContainer                                                         |
| 針對每個 .。。 在 .。。                      | AdsBuildEnumerator () ADsEnumerateNext ()                                |
| 連接、命令、記錄集     | >idirectorysearch                                                      |
| 安全描述項、ACL、ACE      | IADsSecurityDescriptor、IADsAccessControlList、IADsAccessControlEntry |



 

 

 




