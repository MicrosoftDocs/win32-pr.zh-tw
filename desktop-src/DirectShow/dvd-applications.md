---
description: DVD 應用程式
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: DVD 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d601fdbf94ef2a2d9a70d1f28f68854200b58f9fb44d23c3738994f3001e3a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102958"
---
# <a name="dvd-applications"></a>DVD 應用程式

DirectShow 提供稱為「 [DVD](dvd-navigator-filter.md)導覽器來源篩選」的元件，可簡化 c + + 中的 dvd 導覽工作。 DVD 導覽程式具有您在全功能的獨立 DVD 播放程式上找到的所有功能，加上在個人電腦上播放 Dvd 專用的其他功能。 使用 DVD 導覽器，c + + 和腳本開發人員可以建立功能完整的 DVD 應用程式，而不需參照 DVD 規格。 與解碼器篩選器協調的 DVD 導覽器，也會處理 (CSS 和類比禁止複製) 的區域管理和著作權保護，讓應用程式開發人員與這些詳細資料隔離。

DVD 導覽器篩選器可在整個 DVD-Video 磁片區上運作，而這是由 VIDEO TS 目錄中的檔案所組成 \_ 。 不同于使用個別資料流程或檔案的大部分 DirectShow 來源篩選，DVD 導覽器會使用標題、章節和時間代碼的 DVD-Video 結構。 如果開發人員想要在 DirectShow 中播放個別的 mpeg-2 檔案，則應該使用[mpeg-2 的信號](mpeg-2-demultiplexer.md)，而不是使用 DVD 瀏覽器篩選器。 如需詳細資訊，請參閱[DirectShow 中的 mpeg-2 支援](mpeg-2-support-in-directshow.md)。

> [!Note]  
> 若要播放 Dvd，使用者必須具有 MPEG-2 解碼器。

 

此章節包含下列主題。

-   [DirectShow 中的 DVD 支援功能](dvd-support-features-in-directshow.md)
-   [DVD 基本概念](dvd-basics.md)
-   [建立 DVD 篩選器 Graph](building-the-dvd-filter-graph.md)
-   [取得 DVD 介面指標](obtaining-the-dvd-interface-pointers.md)
-   [DVD 命令](dvd-commands.md)
-   [識別有效的 DVD 作業](identifying-valid-dvd-operations.md)
-   [同步處理 DVD 命令](synchronizing-dvd-commands.md)
-   [DVD 導覽器中的資料 Flow](data-flow-in-the-dvd-navigator.md)
-   [處理 DVD 事件通知](handling-dvd-event-notifications.md)
-   [使用 DVD 功能表](working-with-dvd-menus.md)
-   [音訊和子圖片串流](audio-and-subpicture-streams.md)
-   [強制執行家長管理層級](enforcing-parental-management-levels.md)
-   [儲存和還原 DvdState 物件](saving-and-restoring-dvdstate-objects.md)
-   [使用 DVD 文字字串](working-with-dvd-text-strings.md)
-   [播放卡拉卡拉的音訊串流](playing-karaoke-audio-streams.md)
-   [處理光碟 Ejections](handling-disc-ejections.md)
-   [Windows Vista 中的 DVD 播放增強功能](dvd-playback-enhancements-in-windows-vista.md)
-   [DVD 篩選 Graph 設定](dvd-filter-graph-configuration.md)
-   [C + + DVD 參考頁面的快捷方式](shortcuts-to-c-dvd-reference-pages.md)

如需有關 DVD/MPEG2 解碼器開發的參考，請參閱[DirectShow 中的 Dvd 解碼器開發](dvd-decoder-development-in-directshow.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow](using-directshow.md)
</dt> </dl>

 

 



