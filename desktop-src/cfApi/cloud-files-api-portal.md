---
description: 雲端篩選 API 會在使用者模式與檔案系統之間的界限提供功能。
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: 雲端同步引擎
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: debe32a1849a393a067017f90f5405c4b3ba77d1
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "106985729"
---
# <a name="cloud-sync-engines"></a>雲端同步引擎

另請參閱 [雲端鏡像範例](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample)。

從 Windows 10 版本1709開始，Windows 提供雲端檔案 *API*。 此 API 是由數個原生 Win32 和 WinRT Api 所組成，可將雲端同步引擎的支援正規化，並處理工作，例如建立和管理預留位置檔案和目錄。 此 API 的使用者通常是同步處理提供者，以及某些範圍的 Windows 應用程式。

## <a name="in-this-section"></a>本節內容

| 主題                                                                | 描述                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [建立支援預留位置檔案的雲端同步處理引擎](build-a-cloud-file-sync-engine.md)<br/> | 瞭解如何使用雲端檔案 API 來建立包含預留位置檔案和檔案總管整合的雲端檔案同步處理引擎。 <br/> |
| [雲端篩選參考](cloud-filter-reference.md)<br/> | 雲端篩選 API 是原生 WIN32 API，屬於更廣泛的雲端檔案 API。 雲端篩選 API 會在使用者模式與檔案系統之間的界限提供功能。 此 API 會處理預留位置檔案和目錄的建立和管理。 <br/> |

