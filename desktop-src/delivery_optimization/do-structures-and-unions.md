---
title: 進行結構和等位
description: 傳遞最佳化 (執行) 介面會使用下列結構。
ms.assetid: 58A5361E-871A-4911-85BD-83F18CB9A2F5
ms.topic: article
ms.date: 07/03/2019
ms.openlocfilehash: 860672e72e1e5f134382fd46cd9b36d1d411361e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092976"
---
# <a name="do-structures-and-unions"></a>進行結構和等位

傳遞最佳化 (執行) [介面](do-interfaces.md) 會使用下列結構。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**BG_FILE_PROGRESS**](bg-file-progress.md) | **BG_FILE_PROGRESS** 結構會提供檔案相關的進度資訊，例如已傳送的位元組數目。 |
| [**BG_FILE_RANGE**](bg-file-range.md) | **BG_FILE_RANGE** 結構會識別要從檔案下載的位元組範圍。 |
| [**BG_JOB_PROGRESS**](bg-job-progress.md) | **BG_JOB_PROGRESS** 結構會提供作業相關的進度資訊，例如已傳送的位元組和檔案數目。 針對上傳作業，進度會套用至上傳檔案，而不是回復檔。  |
| [**BG_JOB_TIMES**](bg-job-times.md) | **BG_JOB_TIMES** 結構會提供作業相關的時間戳記。 |
| [**BITS_FILE_PROPERTY_VALUE**](bits-file-property-value.md) | **BITS_FILE_PROPERTY_VALUE** 聯集會根據 [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)列舉中的值，提供 DO 檔案的屬性值。 |
| [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) | **BITS_JOB_PROPERTY_VALUE** 聯集會根據 [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)列舉值，提供 DO 作業的屬性值。 |
| [**DO_DOWNLOAD_ENUM_CATEGORY**](./do/ns-do-do_download_enum_category.md) | 由 **IDOManager：： EnumDownloads** 用來依特定屬性的值篩選下載列舉。 |
| [**DO_DOWNLOAD_RANGE**](./deliveryoptimizationdownloadtypes/ns-deliveryoptimizationdownloadtypes-do_download_range.md) | 識別要從檔案下載的單一位元組範圍。 |
| [**DO_DOWNLOAD_RANGE_INFO**](./do/ns-do-do_download_range_info.md) | 識別要從檔案下載的位元組範圍陣列。 |
| [**DO_DOWNLOAD_STATUS**](./do/ns-do-do_download_status.md) | 用來取得特定下載的狀態。 |
| [**DOSwarmStats**](doswarmstats.md) | 包含用來下載和上傳檔案之統計資料的欄位。 |