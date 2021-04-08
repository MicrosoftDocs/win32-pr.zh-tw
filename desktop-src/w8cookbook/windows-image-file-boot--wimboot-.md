---
title: 'Windows 映像檔案開機 (的 WimBoot) '
description: 'Windows 映像檔案開機 (的 WimBoot) '
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "103684193"
---
# <a name="windows-image-file-boot-wimboot"></a>Windows 映像檔案開機 (的 WimBoot) 

## <a name="platform"></a>平台

**用戶端：** Windows 8.1  

## <a name="description"></a>Description

WimBoot 是 Oem 部署 Windows 的另一種方式。 WimBoot 部署會從壓縮的 Windows 映像檔案中，直接啟動並執行 Windows (WIM) 。 此 WIM 檔案是不可變的，且其存取權是由新的檔案系統篩選器驅動程式 (WoF.sys) 所管理。

結果是安裝 Windows 所需的磁碟空間大幅減少。

## <a name="manifestations"></a>表現

大部分的應用程式應該完全不會受到 WimBoot 的影響。 只有存取和解除鎖定系統檔案或預先載入之檔案的應用程式可能會受到影響。 由於 WIM 是不可變的，因此 (也就是系統或預先載入的檔案) 的更新，只會儲存在 C： \\ 磁碟分割上。

如果應用程式解除鎖定所有 WIM 型系統和預先載入之檔案的寫入存取權，則 WimBoot 提供的節省將會完全遺失，因為這些檔案都將解壓縮並放在 C：磁片區上 \\ 。

此外，備份與還原應用程式必須留意到 WimBoot 部署，因為 WIM 存在於不同的磁碟分割;也就是說，在備份時， \\ 必須儲存 C：和 WIM 磁碟分割，而且兩者都必須一起還原。

## <a name="solution"></a>解決方法

引進新的 Api，可讓應用程式直接查詢指定的磁片區或檔案是否受 WIM 支援。 這項資訊可讓應用程式做出適當的決策，例如僅針對讀取權限開啟這些檔案，或識別必須一起備份和還原的磁片區/磁碟分割。

## <a name="compatibility-performance-reliability-or-usability-tests"></a>相容性、效能、可靠性或可用性測試

應用程式開發人員應該在 WimBoot 系統上測試其軟體及其對應的案例，特別是當這些應用程式存取系統或預先載入的檔案時。 在完成案例後，請特別注意，以大幅減少可用磁碟空間。

 

 




