---
description: 撰寫64位合併模組時，請遵循這些指導方針。
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: 使用64位合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693844"
---
# <a name="using-64-bit-merge-modules"></a>使用64位合併模組

64位合併模組具有此主題中所識別的任何特性。

-   合併模組至少包含一個已針對64位作業系統編譯的元件。
-   Merge 模組不包含64位元件，但僅供 [64 位 Windows Installer](64-bit-windows-installer-packages.md) 套件使用。

合併模組可如下所示使用：

-   64位合併模組可以合併至 [64 位 Windows Installer](64-bit-windows-installer-packages.md) 套件。 合併模組和 Windows Installer 封裝中的 [**範本摘要**](template-summary.md) 屬性必須設定為相同類型的64位處理器。 X64 合併模組只能合併為 x64 封裝，且 Intel64 合併模組只能合併到 Intel64 封裝中。
-   32位合併模組可以合併至32位或 [64 位 Windows Installer](64-bit-windows-installer-packages.md) 套件。
-   64位合併模組可以合併到32位作業系統上的64位封裝中。

撰寫64位合併模組時，請遵守下列各項：

-   使用與撰寫32位合併模組時相同的一般程式。 如需詳細資訊，請參閱 [關於合併模組](about-merge-modules.md) 和 [撰寫合併模組](authoring-merge-modules.md)。
-   如果執行 Intel64 系統，您必須使用 Intel64 值設定 [**範本摘要**](template-summary.md) 屬性。 如果您執行的是 x64 系統，就必須以 x64 值設定 **範本摘要** 屬性。 如需詳細資訊，請參閱 [合併模組摘要資訊資料流程參考](merge-module-summary-information-stream-reference.md)。
-   當相同元件的32位和64位合併模組同時存在時，建議模組具有不同的簽章。 這會讓套件包含元件的兩個版本。

如需詳細資訊，請參閱 [64 位作業系統上的 Windows Installer](windows-installer-on-64-bit-operating-systems.md)。

 

 



