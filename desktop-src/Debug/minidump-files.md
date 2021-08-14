---
description: 應用程式可以產生使用者模式小型傾印檔案，其中包含損毀傾印檔案中包含的有用資訊子集。
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: 小型傾印檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412e719d54f34c9766981667be35990c37ae3511eaecc8836ceac0311a5105e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406088"
---
# <a name="minidump-files"></a>小型傾印檔案

應用程式可以產生使用者模式小型傾印檔案，其中包含損毀傾印檔案中包含的有用資訊子集。 應用程式可以非常快速且有效率地建立小型傾印檔案。 因為小型傾印檔案很小，所以可以輕鬆地透過網際網路傳送給應用程式的技術支援。

小型傾印檔案未包含完整損毀傾印檔案的資訊，但它包含足夠的資訊來執行基本的調試作業。 若要讀取小型傾印檔案，您必須有可供偵錯工具使用的二進位檔和符號檔。

目前版本的 Microsoft Office 和 Microsoft Windows 建立小型傾印檔案，以在客戶的電腦上分析失敗的目的。

下列 DbgHelp 函式可用於小型傾印檔案。

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



