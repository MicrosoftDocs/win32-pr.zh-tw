---
description: 一般情況下，偵錯工具的資訊會儲存在與可執行檔分開的符號檔中。
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: 符號檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 610e289a64ed807a26086f12780b45bc35ea65464946ec81a07e4169515d1132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642178"
---
# <a name="symbol-files"></a>符號檔

一般情況下，偵錯工具的資訊會儲存在與可執行檔分開的符號檔中。 這項偵錯工具資訊的執行已經過多年的改變，而下列檔將提供有關這些各種不同實施的指引。

## <a name="pdb-files"></a>PDB 檔案

所有新式版本的 Microsoft 編譯器都會將編譯的可執行檔的偵錯工具儲存在個別的 *程式資料庫* 中， ( .pdb) 檔。 這個檔案通常稱為 *PDB*。 資料會儲存在可執行檔的個別檔案中，以協助限制可執行檔的大小、節省磁片儲存空間，並減少載入資料所需的時間。 這種方法也可以散發可執行檔，而不需要洩漏這項重要資訊，讓程式更容易進行反向工程。

若要建立 PDB，請根據您的組建工具的指示，建立您的可執行檔以及偵錯工具的相關資訊。

DbgHelp API 可以使用 Pdb 來取得下列資訊。

-   publics 和匯出
-   全域符號
-   本機符號
-   型別資料
-   原始程式檔
-   行號

## <a name="dbg-files-and-embedded-debug-information"></a>DBG 檔案和內嵌的調試資訊

舊版的 Microsoft 工具組是用來將偵錯工具內嵌到可執行檔中，但通常會將它從副檔名為 dbg 的個別檔案中移除。 這通常稱為 *DBG* 檔案。 DBG 檔案使用的 PE 檔案格式與可執行檔相同。

DBGs 和內嵌偵錯工具的 DbgHelp API 支援受到限制，並且包含下列內容。

-   publics 和匯出
-   全域符號

 

 



