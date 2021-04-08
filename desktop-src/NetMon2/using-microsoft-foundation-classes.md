---
description: 由於靜態連結 Dll 的使用量，您應該避免使用 Microsoft Foundation 類別 (MFCs) 撰寫專家。
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: 使用 Microsoft Foundation 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097c4baea2ec109933d52eed420042528e9eea76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693716"
---
# <a name="using-microsoft-foundation-classes"></a>使用 Microsoft Foundation 類別

由於靜態連結 Dll 的使用量，您應該避免使用 Microsoft Foundation 類別 (MFCs) 撰寫專家。 但是，如果您使用 MFC，請在進入時立即加入下列程式碼，以確保存取任何 MFC DLL 資源：

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



