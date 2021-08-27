---
title: '新功能 (IMAPI.EXE) '
description: 下表指出每個映射主控 API 版本的新功能。
ms.assetid: a90daec2-5916-4c24-b2ad-94199641a2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a3b0ceb966f3f6db6583b86b616608da3bee4f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472174"
---
# <a name="whats-new-image-mastering-api"></a>新功能：映射主控 API

下表指出每個映射主控 API 版本的新功能。




| 版本 | 功能描述 | 
|---------|-------------------------|
| 版本2。0 | 大部分的 API 都經過重新設計。 版本2.0 仍提供大部分的1.0 版功能。 我們鼓勵這些撰寫映射主控應用程式或執行新的裝置和格式開發，以使用版本2.0，而不是1.0 版。<br /> imapi.exe 2.0 包含在 Windows Vista 中。 啟用 Windows XP 和 Windows Server 2003 的相同功能需要安裝<a href="https://support.microsoft.com/kb/932716">KB932716</a>更新套件。<br /> Point-Release 附注：<br /><ul><li>Windows Vista Service Pack 1 (SP1) 和 Windows Server 2008 中引進了透過<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a>介面提供多重開機支援的更新。<br /></li><li>功能更新供應專案可支援 BD-R\BD-RE 格式、原始 CD 映射建立，以及<a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05">儲存體的 Windows feature Pack</a>中包含燒錄驗證。 Windows Vista sp1、Windows XP Service pack 2 (SP2) 和更新版本，以及 Windows Server 2003 （含 service pack 1） (SP1) 和更新版本都支援此功能更新。 此外，這些功能包含在 Windows 7 和 Windows Server 2008 中。<br /></li><li>Windows 7 和 Windows Server 2008 原生的 imapi.exe 2.0 功能包括音訊 cd 的「Gapless 燒錄」，以及在燒錄作業期間刪除「雙隱藏」。 雙隱藏是在較大的燒錄作業內進行的程式，在此作業中，每個檔案在燒錄到光碟之前都隱藏。使用最新版本的 IMAPI.EXE 2.0 時，會選擇性地選擇隱藏的檔案，並將其餘的檔案 (大部分的大型檔案) 非隱藏。 最終結果會儲存磁碟空間和作業時間。<br /></li></ul> | 
| 版本 1.0 | 初始版本。 讓應用程式階段，並將簡單的音訊或資料影像燒錄到 CD-R 和 cd-rw 裝置。 API 支援 Redbook 音訊和資料光碟的 Joliet 和 ISO 9660 格式。 如需1.0 版的相關資訊，請參閱<a href="imapiv1.md">IMAPIv1 支援</a>。包含在 Windows XP 中。<br /> | 




 

## <a name="version-20"></a>版本2。0

-   允許應用程式燒錄至 DVD-R、DVD + R、DVD RW、DVD + RW、DVD + DL、DVD DL 和 DVD-ROM、bd 和 BD 媒體格式。
-   允許同時錄製至多個磁片磁碟機。 在1.0 版中，IMAPI.EXE 一次只能使用一部系統上的燒錄機。 如果您在 Windows Vista 上執行1.0 版的應用程式，其他應用程式可能會同時在系統中的其他磁片磁碟機上使用 imapi.exe 1.0 或2.0 介面。 雖然這通常會被視為一項優點，但依賴單一系統燒錄機行為的應用程式可能需要較小的更新。
-   當錄製器將資訊寫入光碟時，會拒絕對錄製器的存取。否則，此錄製器可供其他用戶端使用。
-   在用戶端電腦上支援一個以上的隱藏檔案，而版本1.0 只允許一個全系統的隱藏檔案。
-   在 Windows Vista 中，1.0 版不再包含服務或核心模式的元件。 不過， [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) 介面仍會使用 ioctl 磁片 \_ \_ 獨佔 \_ 存取，而 ioctl \_ SCSI \_ 會 \_ 透過 \_ 直接命令傳遞，以管理特定磁片磁碟機裝置的存取或通訊。
-   在 Windows Vista 上，版本1.0 介面現在會呼叫2.0 版介面。
-   隨附于 Windows Vista SP1 和 Windows Server 2008 中的 imapi.exe 版本2.0 透過 [**IFileSystemImage2**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2)介面提供多重開機支援。
-   允許針對音訊 Cd 使用「Gapless 燒錄」。 使用 Gapless 燒錄，可以移除音訊播放軌之間的聲音間距。
-   已將 ' Double 隱藏 ' 取代為特別選取檔案進行隱藏的處理常式，並將其餘的檔案保留 (大部分的大型檔案) 非隱藏。 最終結果會儲存磁碟空間和作業時間。
-   使用 [儲存體的 Windows Feature Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)，可透過 [**IBurnVerification**](/windows/desktop/api/imapi2/nn-imapi2-iburnverification)存取的屬性提供燒錄驗證選項。
