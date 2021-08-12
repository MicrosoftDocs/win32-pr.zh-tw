---
description: 雲端篩選 API 會在使用者模式與檔案系統之間的界限提供功能。
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: 雲端同步引擎
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: 39dd28779c07dfd6e44fde0e53f583e72971d5883205f42581e3b5ac4102c0eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551372"
---
# <a name="cloud-sync-engines"></a>雲端同步引擎

另請參閱 [雲端鏡像範例](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample)。

從 Windows 10 版本1709開始，Windows 提供雲端檔案 *API*。 此 API 是由數個原生 Win32 和 WinRT Api 所組成，可將雲端同步引擎的支援正規化，並處理工作，例如建立和管理預留位置檔案和目錄。 此 API 的使用者通常是同步處理提供者，而 Windows 應用程式的範圍。

## <a name="in-this-section"></a>本節內容

| 主題                                                                | 描述                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [建立支援預留位置檔案的雲端同步處理引擎](build-a-cloud-file-sync-engine.md)<br/> | 瞭解如何使用雲端檔案 API 來建立包含預留位置檔案和檔案總管整合的雲端檔案同步處理引擎。 <br/> |
| [雲端篩選參考](cloud-filter-reference.md)<br/> | 雲端篩選 API 是原生 WIN32 API，屬於更廣泛的雲端檔案 API。 雲端篩選 API 會在使用者模式與檔案系統之間的界限提供功能。 此 API 會處理預留位置檔案和目錄的建立和管理。 <br/> |