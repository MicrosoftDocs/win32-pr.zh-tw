---
description: 下列範例會使用 SetStringInBlob 函數來建立特殊的 BLOB 專案。
ms.assetid: 4a921b0d-9934-48e2-8837-be0bd7b7fa7a
title: 特殊 BLOB 專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfc40029e0a0f88c2f7bd242881b0d750a5dfa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690764"
---
# <a name="special-blob-entries"></a><span data-ttu-id="8f7fa-103">特殊 BLOB 專案</span><span class="sxs-lookup"><span data-stu-id="8f7fa-103">Special BLOB Entries</span></span>

<span data-ttu-id="8f7fa-104">下列範例會使用 [**SetStringInBlob**](setstringinblob.md) 函數來建立特殊的 BLOB 專案。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-104">The following examples use the [**SetStringInBlob**](setstringinblob.md) function to create special BLOB entries.</span></span>

## <a name="npp-name"></a><span data-ttu-id="8f7fa-105">NPP 名稱</span><span class="sxs-lookup"><span data-stu-id="8f7fa-105">NPP Name</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a><span data-ttu-id="8f7fa-106">NPP 類別識別碼</span><span class="sxs-lookup"><span data-stu-id="8f7fa-106">NPP Class Identifier</span></span>

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a><span data-ttu-id="8f7fa-107">CFGPROC 程式名稱</span><span class="sxs-lookup"><span data-stu-id="8f7fa-107">CFGPROC Procedure Name</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a><span data-ttu-id="8f7fa-108">Finder UI 的樹狀目錄根名稱</span><span class="sxs-lookup"><span data-stu-id="8f7fa-108">Tree Root Name for Finder UI</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a><span data-ttu-id="8f7fa-109">搜尋工具 UI 的顯示字串</span><span class="sxs-lookup"><span data-stu-id="8f7fa-109">Display String for Finder UI</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a><span data-ttu-id="8f7fa-110">介面標記</span><span class="sxs-lookup"><span data-stu-id="8f7fa-110">Interface Tags</span></span>

<span data-ttu-id="8f7fa-111">此範例包含 NPP 所支援的每個介面。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-111">This example includes every interface supported by the NPP.</span></span>

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



