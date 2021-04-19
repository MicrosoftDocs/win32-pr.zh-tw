---
title: 在 IDL 檔案中使用新的資料類型
description: Basetsd .h 標頭檔會定義撰寫在32和64位 Windows 上執行之應用程式所需的新資料類型。
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Basetsd .h 標頭檔 64-位 Windows 程式設計
- IDL 檔案64位 Windows 程式設計中的資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff1add2d70c99069911ac76ad168b7d31c3365f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967487"
---
# <a name="using-new-data-types-in-your-idl-file"></a><span data-ttu-id="b84d4-105">在 IDL 檔案中使用新的資料類型</span><span class="sxs-lookup"><span data-stu-id="b84d4-105">Using New Data Types in Your IDL File</span></span>

<span data-ttu-id="b84d4-106">Basetsd .h 標頭檔會定義撰寫在32和64位 Windows 上執行之應用程式所需的新資料類型。</span><span class="sxs-lookup"><span data-stu-id="b84d4-106">The Basetsd.h header file defines the new data types needed for writing applications that run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="b84d4-107">若要在您的介面中使用這些資料類型，請將 Basetsd 匯入至 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="b84d4-107">To use these data types in your interfaces, import Basetsd.h into your IDL file.</span></span> <span data-ttu-id="b84d4-108">請勿包含檔案， \# 或在編譯時期最後會有多個定義。</span><span class="sxs-lookup"><span data-stu-id="b84d4-108">Do not \#include the file or you will end up with multiple definitions at compile time.</span></span>

<span data-ttu-id="b84d4-109">或者，您也可以在 IDL 檔案中包含或匯入 Basetsd .idl 檔。</span><span class="sxs-lookup"><span data-stu-id="b84d4-109">Alternatively, you can include or import the Basetsd.idl file into your IDL file.</span></span>

<span data-ttu-id="b84d4-110">如需將系統標頭檔新增至 IDL 檔案的詳細資訊，請參閱匯 [入檔案和型別程式庫](/windows/desktop/Midl/importing-files-and-type-libraries) 和匯 [入系統標頭檔](/windows/desktop/Midl/importing-system-header-files)。</span><span class="sxs-lookup"><span data-stu-id="b84d4-110">For more information on adding system header files to your IDL file, see [Importing Files and Type Libraries](/windows/desktop/Midl/importing-files-and-type-libraries) and [Importing System Header Files](/windows/desktop/Midl/importing-system-header-files).</span></span>

 

 