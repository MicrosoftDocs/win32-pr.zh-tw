---
description: 由於靜態連結 Dll 的使用量，您應該避免使用 Microsoft Foundation 類別 (MFCs) 撰寫專家。
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: 使用 Microsoft Foundation 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec1b01260d3fd7d1e7058c9fff8aa3cc32390b3f2f6cc715c91563a871fbf20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362927"
---
# <a name="using-microsoft-foundation-classes"></a>使用 Microsoft Foundation 類別

由於靜態連結 Dll 的使用量，您應該避免使用 Microsoft Foundation 類別 (MFCs) 撰寫專家。 但是，如果您使用 MFC，請在進入時立即加入下列程式碼，以確保存取任何 MFC DLL 資源：

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



