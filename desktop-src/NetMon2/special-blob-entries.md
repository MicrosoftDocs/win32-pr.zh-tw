---
description: 下列範例會使用 SetStringInBlob 函數來建立特殊的 BLOB 專案。
ms.assetid: 4a921b0d-9934-48e2-8837-be0bd7b7fa7a
title: 特殊 BLOB 專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0659fa05219dcc715c6c00b3d28635e2500f73e4e5bece72049ee43839a0820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363136"
---
# <a name="special-blob-entries"></a>特殊 BLOB 專案

下列範例會使用 [**SetStringInBlob**](setstringinblob.md) 函數來建立特殊的 BLOB 專案。

## <a name="npp-name"></a>NPP 名稱

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a>NPP 類別識別碼

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a>CFGPROC 程式名稱

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a>Finder UI 的樹狀目錄根名稱

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a>搜尋工具 UI 的顯示字串

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a>介面標記

此範例包含 NPP 所支援的每個介面。

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



