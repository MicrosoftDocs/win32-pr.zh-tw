---
description: 具有系統管理許可權的使用者和應用程式可以取得和修改系統上 Windows Installer 應用程式和修補程式的網路、URL 和媒體來源清單資訊。
ms.assetid: e8c66bad-f594-4926-b3b4-c8b245dcfa83
title: 管理安裝來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fc45253af20ae5f9792ee3a5ec7dd318c80295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979390"
---
# <a name="managing-installation-sources"></a>管理安裝來源

具有系統管理許可權的使用者和應用程式可以取得和修改系統上 Windows Installer 應用程式和修補程式的網路、URL 和媒體來源清單資訊。

**Windows Installer 2.0：** 不支援。 系統管理員無法讀取、重新排列或取代來源清單中的專案，也無法修改或抓取來源清單屬性。 您可以管理網路來源，但不能管理 URL 或媒體來源。 系統管理員只能針對目前的使用者，管理個別電腦應用程式或安裝為每位使用者之應用程式的來源清單。 這可防止系統管理員使用早于 Windows Installer 版本3.0 的版本，管理系統中所有使用者的來源清單資訊。

**Windows Installer 3.0 和更新版本：** 具有系統管理員許可權的使用者和應用程式，可以針對所有使用者在系統上安裝的 Windows Installer 應用程式和修補程式，取得和修改來源清單資訊。 來源清單函式可以用來管理網路、URL 和媒體來源的來源清單和來源清單屬性。 安裝程式可以重新排列外部進程的來源清單。

具有系統管理許可權的使用者和應用程式，可以讀取和修改下列類型的來源清單資訊：

-   針對系統上的所有使用者安裝的應用程式和修補程式的來源清單。
-   存在於應用程式來源之外之修補程式來源的來源清單。
-   存在於網路來源之外的 URL 和媒體來源的來源清單。
-   來源清單屬性，例如 [**MEDIAPACKAGEPATH**](mediapackagepath.md)、 [**DiskPrompt**](diskprompt.md)、 **LastUsedSource**、 **LastUsedType** 和 **PackageName**。

來源清單函式可以藉由指定安裝內容和使用者內容，限制找到的來源清單範圍。 有三種可能的安裝內容：每位使用者 (非受控) 、每部電腦，以及每位使用者管理。 使用者內容可以是系統上的特定使用者或所有使用者。

非系統管理員無法修改存在於其他使用者的每個使用者 (受控或非受控) 內容中之應用程式或修補程式實例的來源清單。 非系統管理員可以修改下列內容所安裝之應用程式或修補程式實例的來源清單：

-   自己的每位使用者 (非受控) 內容。
-   電腦內容，但只有在 [DisableBrowse](disablebrowse.md)、 [AllowLockdownBrowse](allowlockdownbrowse.md)和 [AlwaysInstallElevated](alwaysinstallelevated.md) 原則允許它們流覽應用程式或修補程式來源時才會提供。
-   他們自己的每個使用者管理內容，但只有在 [DisableBrowse](disablebrowse.md)、 [AllowLockdownBrowse](allowlockdownbrowse.md)和 [AlwaysInstallElevated](alwaysinstallelevated.md) 原則允許他們流覽應用程式或修補程式來源時才可使用。

系統管理員可以修改非系統管理員可以修改的任何來源清單。 此外，具有系統管理許可權的系統管理員和應用程式，可以修改下列內容所安裝之應用程式或修補程式的來源清單：

-   每一電腦的內容。
-   他們自己的每位使用者 (非受控) 或自己的個別使用者管理內容。
-   另一位使用者的每個使用者管理內容。

> [!Note]  
> 具有系統管理許可權的使用者和應用程式無法修改個別使用者 (非受控) 內容中所安裝之應用程式或修補程式實例的來源清單。

 

## <a name="managing-network-and-url-sources-for-products-and-patches"></a>管理產品和修補程式的網路和 URL 來源

您可以使用 [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) 函式，針對特定內容中的修補程式或應用程式，新增或重新排序網路和 URL 來源的來源清單。 使用 *dwCoNtext* 參數來指定安裝內容。 使用 *szUserSid* 參數來指定使用者內容。

您可以使用 [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) 函式，針對尚未套用至指定內容中任何應用程式的修補程式建立來源清單。 當註冊 patch 以擁有較高的許可權時，這會很有用。 如需有關為修補程式註冊更高許可權的詳細資訊，請參閱 [修補 Per-User 受控應用程式](patching-per-user-managed-applications.md)。

您可以使用 [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea) 函式，在指定的內容中移除應用程式或修補程式的現有來源。 移除應用程式或修補程式的目前來源，會強制安裝程式在下次需要來源時搜尋來源清單中的來源。

您可以使用 [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) 函式來列舉指定修補程式或應用程式的來源清單中的來源。

## <a name="managing-media-sources-for-products-and-patches"></a>管理產品和修補程式的媒體來源

使用 [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska) 函式來新增或更新已註冊之應用程式或修補程式之媒體來源的磁片資訊。 每個專案都是以磁片識別碼來唯一識別。 如果磁片已存在，則會以新的磁片區標籤和磁片提示值進行更新。 如果磁片不存在，就會以新的值建立新的磁片專案。

您可以使用 [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska) 函式，在特定內容中，針對應用程式或修補程式的媒體來源，移除現有的已註冊磁片。

使用 [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) 函式來列舉針對應用程式或修補程式，在媒體來源下註冊的磁片清單。

## <a name="retrieval-and-modification-of-source-list-information"></a>提取和修改來源清單資訊

您可以使用 [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) 和 [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) 函式來抓取或修改特定內容中，應用程式或修補程式的來源清單相關資訊。 使用 *dwCoNtext* 參數來指定安裝內容。 使用 *szUserSid* 參數來指定使用者內容。

可以存取來源清單屬性，例如 [**MEDIAPACKAGEPATH**](mediapackagepath.md)、 [**DiskPrompt**](diskprompt.md)、 **LastUsedSource**、 **LastUsedType** 和 **PackageName** 。

> [!Note]  
> 只能讀取 **LastUsedType** 來源清單屬性。 無法使用 [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) 函數直接設定。

 

## <a name="clearing-the-complete-source-list-or-forcing-a-source-resolution"></a>清除完整來源清單或強制進行來源解析

您可以使用 [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa) 函式，針對指定的應用程式或 patch 實例，移除指定來源類型的所有現有來源。 如果相同內容中的任何應用程式未安裝修補程式，也會移除修補註冊。 使用 *dwCoNtext* 參數來指定安裝內容。 使用 *szUserSid* 參數來指定使用者內容。

使用 [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) 清除在指定的內容中，應用程式或修補程式的上次使用來源專案。 此函式會移除名為 **LastUsedSource** 的屬性註冊。 此函數不會影響已註冊的來源清單。 清除 **LastUsedSource** 註冊會強制安裝程式在下次需要來源時，對已註冊的來源進行來源解析。

 

 



