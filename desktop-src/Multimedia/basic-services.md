---
title: 基本服務
description: 基本服務
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- 多媒體檔案 i/o，基本服務
- 檔案 i/o、基本服務
- 輸入和輸出 (i/o) ，基本服務
- I/o (輸入和輸出) 、基本服務
- 基本 i/o
- mmioOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ef4ea778ad0c84137aa75d36f46dc30310180c69416a1240078f01e53d6931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145121"
---
# <a name="basic-services"></a>基本服務

使用基本的 i/o 服務，類似于使用 C 執行時間程式庫的執行時間檔案 i/o 服務。 必須先開啟檔案，才能讀取或寫入檔案。 讀取或寫入之後，必須關閉檔案。 您也可以在開啟的檔案內變更目前的讀取或寫入位置。

在您開始對檔案進行任何 i/o 作業之前，必須先使用 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 函式來開啟檔案。 此函數會傳回 **HMMIO** 類型的檔案控制代碼。 呼叫其他檔案 i/o 函式時，您可以使用此檔案控制代碼來識別開啟的檔案。

> [!Note]  
> **HMMIO** 檔案控制代碼不是標準檔案控制代碼。 請勿搭配 Win32 或 C 執行時間檔案 i/o 函數使用 **HMMIO** 檔案控制代碼。

 

當您使用 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 開啟檔案時，您可以使用旗標來指定是否要開啟它以進行讀取、寫入或兩者。 您也可以指定旗標，讓您建立或刪除檔案。 當您完成讀取或寫入檔案時，請使用 [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) 函數來關閉檔案。

您可以分別使用 [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) 和 [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) 函數來讀取和寫入檔案。 下一個讀取或寫入作業會發生在檔案中目前的檔案位置或檔案指標。 每次讀取或寫入檔案時，目前的檔案位置都是 advanced。

您也可以使用 [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) 函數來變更目前的檔案位置。 您應確定在檔案中指定有效的位置。 如果您指定了不正確位置，例如超過檔案結尾， **mmioSeek** 可能不會傳回錯誤，但後續的 i/o 作業可能會失敗。

您可以針對基本檔案 i/o 以外的作業使用 **mmioOpen** 函式的旗標。 例如，您可以藉由指定 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) 結構來開啟記憶體檔案、指定自訂的 i/o 程式，或為緩衝的 i/o 提供緩衝區。

 

 