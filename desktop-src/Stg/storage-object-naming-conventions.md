---
title: 儲存體物件命名慣例
description: 儲存體和資料流程物件是根據一組慣例來命名。
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- 結構化儲存體 Strctd Stg.、基本概念、儲存物件命名慣例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e828674f4165bdb54dc2ec06748ab4165e75e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371929"
---
# <a name="storage-object-naming-conventions"></a><span data-ttu-id="41072-104">儲存體物件命名慣例</span><span class="sxs-lookup"><span data-stu-id="41072-104">Storage Object Naming Conventions</span></span>

<span data-ttu-id="41072-105">儲存體和資料流程物件是根據一組慣例來命名。</span><span class="sxs-lookup"><span data-stu-id="41072-105">Storage and stream objects are named according to a set of conventions.</span></span>

<span data-ttu-id="41072-106">根儲存物件的名稱是基礎檔案系統中的實際檔案名。</span><span class="sxs-lookup"><span data-stu-id="41072-106">The name of a root storage object is the actual name of the file in the underlying file system.</span></span> <span data-ttu-id="41072-107">它符合檔案系統所強加的慣例和限制。</span><span class="sxs-lookup"><span data-stu-id="41072-107">It conforms to the conventions and restrictions that the file system imposes.</span></span> <span data-ttu-id="41072-108">傳遞至儲存相關方法和函式的檔案名字串，會以不會的方式傳遞至檔案系統。</span><span class="sxs-lookup"><span data-stu-id="41072-108">File name strings passed to storage-related methods and functions are passed on, uninterpreted and unchanged, to the file system.</span></span>

<span data-ttu-id="41072-109">儲存物件內所包含之嵌套專案的名稱是由特定儲存物件的執行所管理。</span><span class="sxs-lookup"><span data-stu-id="41072-109">The name of a nested element contained within a storage object is managed by the implementation of the particular storage object.</span></span> <span data-ttu-id="41072-110">所有儲存體物件的執行都必須支援長度為32個字元的嵌套元素名稱 (包括 Null 結束字元) ，不過某些實 **值** 可能會支援較長的名稱。</span><span class="sxs-lookup"><span data-stu-id="41072-110">All implementations of storage objects must support nested element names 32 characters in length (including the **NULL** terminator), although some implementations might support longer names.</span></span> <span data-ttu-id="41072-111">儲存物件是否執行任何大小寫轉換都是實作為定義。</span><span class="sxs-lookup"><span data-stu-id="41072-111">Whether the storage object does any case conversion is implementation-defined.</span></span> <span data-ttu-id="41072-112">如此一來，定義專案名稱的應用程式必須選擇是否執行大小寫轉換時可接受的名稱。</span><span class="sxs-lookup"><span data-stu-id="41072-112">As a result, applications that define element names must choose names that are acceptable whether or not case conversion is performed.</span></span> <span data-ttu-id="41072-113">複合檔案的 COM 執行支援最大長度為32個字元的名稱，且不會執行任何大小寫轉換。</span><span class="sxs-lookup"><span data-stu-id="41072-113">The COM implementation of compound files supports names with a maximum length of 32 characters, and does not perform any case conversion.</span></span>

 

 




