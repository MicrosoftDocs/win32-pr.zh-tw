---
description: 已知的資料夾系統會提供一種方式，讓您與 Windows 中預設存在的某些高階設定檔資料夾互動。
ms.assetid: 8b6163b5-e152-47c2-99f1-43e80cf0713e
title: 使用應用程式中的已知資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0981d354e49f569dda229fab32308d8f4a79ff99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468589"
---
# <a name="working-with-known-folders-in-applications"></a>使用應用程式中的已知資料夾

已知的資料夾系統會提供一種方式，讓您與 Windows 中預設存在的某些高階設定檔資料夾互動。 它也允許應用程式與安裝並向已知資料夾系統註冊的資料夾進行相同的互動。 本主題討論已知的資料夾 Api 提供的可能互動。

-   [已知的資料夾介面](#known-folder-interfaces)
-   [重新導向](#redirection)
-   [相關主題](#related-topics)

> [!IMPORTANT]
> 若要將 [檔]、[圖片] 或 [桌面] 資料夾重新導向至 OneDrive，請使用 OneDrive 已知資料夾移動，而不是本文中所述的重新導向方法。 如需詳細資訊，請參閱 [將 Windows 已知資料夾重新導向並移至 OneDrive](/onedrive/redirect-known-folders)。  

## <a name="known-folder-interfaces"></a>已知的資料夾介面

有兩個已知的資料夾介面： [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) 和 [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)。

[**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager) 提供許多關於這些資料夾的一般功能。 它的方法可讓您：

-   根據該資料夾的 [**KNOWNFOLDERID**](knownfolderid.md)、其正式名稱、其路徑（以字串表示）或其路徑（以 idlist.txt 表示）來抓取 [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) 。
-   將 CSIDL 轉換為其相等的 [**KNOWNFOLDERID**](knownfolderid.md) ，或將 **KNOWNFOLDERID** 轉換為其舊版 CSIDL 對等專案。
-   向系統註冊或取消註冊已知資料夾。
-   取出在該系統上註冊的所有 [**KNOWNFOLDERID**](knownfolderid.md) 值。
-   將已知資料夾重新導向至新位置。

[**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) 提供一種方法，可讓資料夾藉由提供新的路徑來重新導向。 它的其他方法會取得特定已知資料夾的相關資訊，包括：

-   資料夾的類別：虛擬、固定、通用或每位使用者。
-   資料夾的類型，例如壓縮檔、檔、圖片或使用者檔案。
-   資料夾的 [**KNOWNFOLDERID**](knownfolderid.md) 。
-   資料夾的完整路徑，做為 Idlist.txt 或字串。 也是其父資料夾的相對路徑。
-   資料夾的正式名稱。
-   針對資料夾顯示的工具提示。
-   針對資料夾顯示的圖示。
-   說明其目的和使用的資料夾描述。
-   是否能夠將資料夾重新導向。

[**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) 也會提供一種方法，以根據資料夾來取得 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) 。 這可讓您將資料夾系結至處理常式、比較兩個資料夾，以及抓取資料夾的屬性、顯示名稱和上層資料夾。

## <a name="redirection"></a>重新導向

資料夾重新導向是已知資料夾系統的一項重要功能。 類別通用 KF 類別目錄的所有已知資料夾（一般 [  \_ \_ * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * * * 或 [**每位使用者** KF \_ 類別 \_ PERUSER * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * *）都是可重新導向。 但無法重新導向類別 [**虛擬** KF \_ 類別 \_ 虛擬 * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * * * 或 [ **fixedr** KF \_ 類別 \_ 固定](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category)的資料夾。

您可以將資料夾重新導向至同一部電腦上的其他位置，或重新導向至網路上的位置。 在網路重新導向的情況下，可以透過用戶端快取在本機快取資料夾，以提供離線存取。 但是，即使本機快取存在，也必須透過網路存取重新導向的資料夾本身。

資料夾重新導向不是 Windows Vista 的新功能。 例如，在 Windows XP 中，透過 CSIDL 系統識別的某些資料夾，可以透過呼叫 [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha) 或藉由修改登錄中的 CSIDL 專案來重新導向。 在 Windows Vista 和更新版本中，重新導向應該透過 [**IKnownFolder：： SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath) 或 [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)來完成。

若要判斷是否可以重新導向資料夾，請呼叫 [**IKnownFolder：： GetRedirectionCapabilities**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities)。 如果無法重新導向資料夾，此呼叫可以提供說明。

如果將資料夾重新導向至網路位置，則仍可在其上成功呼叫 [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[已知資料夾範例](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
