---
description: Windows 7 引進了程式庫，即使這些檔案儲存在不同的位置，也能為使用者提供單一且一致的檔案查看。
title: Windows 媒體櫃
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973840"
---
# <a name="windows-libraries"></a>Windows 媒體櫃

Windows 7 引進了程式庫，即使這些檔案儲存在不同的位置，也能為使用者提供單一且一致的檔案查看。 程式庫可以由使用者進行設定和組織，而程式庫可以包含在使用者電腦上找到的資料夾，以及透過網路共用的資料夾。 程式庫會呈現更簡單的基礎儲存系統，因為對使用者而言，程式庫中的檔案和資料夾會顯示在單一視圖中，不論其實際儲存位置為何。

建議在 Windows 7 中撰寫新程式的開發人員使用程式庫做為使用者與程式所使用之檔案進行互動的方法。 在您的程式中使用程式庫，可讓使用者在 Windows 7 中有更簡潔、更簡單且更一致的體驗。

開發人員也應該檢查其現有的程式，並視需要進行更新，以使用程式庫。 因為程式庫不是檔案系統的一部分，所以以檔案系統為基礎的 Api 將無法存取使用者可能已設定的任何程式庫。

目前允許使用者將其內容儲存在不同資料夾或不同電腦上的程式，在新增程式庫支援時，最能發揮最大效益。 程式庫可簡化開發人員和使用者各種儲存位置中的內容管理。

本指南將詳細說明程式庫是什麼、如何進行程式來處理程式庫，以及一些程式可以使用程式庫來改善使用者體驗的方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於程式庫](library-leverage-to-manage-folders.md)
</dt> <dt>

[在您的程式中使用程式庫](library-be-library-aware.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Shell 連結](./links.md)
</dt> <dt>

[已知的資料夾](known-folders.md)
</dt> <dt>

[程式庫描述架構](library-schema-entry.md)
</dt> </dl>

 

 
