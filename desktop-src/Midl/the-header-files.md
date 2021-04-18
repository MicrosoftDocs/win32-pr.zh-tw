---
title: 標頭檔
description: 介面標頭檔 (名稱 .h) 包含以目前 IDL 檔案中的介面定義為基礎的型別定義和函式宣告，以及包含在 \ include 指示詞中的檔案中宣告的所有資料類型和作業。
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- 標頭檔 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ae80877b88d8061769b0d6bd56c13469427fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968440"
---
# <a name="the-header-files"></a><span data-ttu-id="146a9-104">標頭檔</span><span class="sxs-lookup"><span data-stu-id="146a9-104">The Header Files</span></span>

<span data-ttu-id="146a9-105">介面標頭檔 (名稱 .h) 包含以目前 IDL 檔案中的介面定義為基礎的類型定義和函式宣告，以及包含在 include 指示詞內含之檔案中宣告的所有資料類型和作業 \# 。</span><span class="sxs-lookup"><span data-stu-id="146a9-105">The interface header file (Name.h) contains type definitions and function declarations based on the interface definition in the current IDL file, as well as all the data types and operations declared in the files included with the \#include directive.</span></span> <span data-ttu-id="146a9-106">使用匯入指示詞彙入之檔案中的資料類型不會複寫至標頭檔;相反地，所產生的標頭檔會包含自匯入檔案所產生之 H 檔案的包含行。</span><span class="sxs-lookup"><span data-stu-id="146a9-106">Data types from the files imported with the import directive are not replicated to the header file; instead, the generated header file contains an include line to the H file generated from the imported file.</span></span>

<span data-ttu-id="146a9-107">將這個檔案包含在 proxy DLL 的來源檔案中，以及使用該介面的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="146a9-107">Include this file in the source files for the proxy DLL and for client applications that use the interface.</span></span>

<span data-ttu-id="146a9-108">從檔案產生的標頭檔的預設名稱。 .idl 是 File .h。</span><span class="sxs-lookup"><span data-stu-id="146a9-108">The default name for a header file generated from a file.idl is File.h.</span></span> <span data-ttu-id="146a9-109">[**/Header**](-header.md) MIDL 編譯器參數會覆寫介面標頭檔案的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="146a9-109">The [**/header**](-header.md) MIDL compiler switch overrides the default name of the interface header file.</span></span>

 

 




