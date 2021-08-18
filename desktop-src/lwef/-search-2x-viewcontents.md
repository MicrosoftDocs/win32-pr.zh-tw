---
title: ViewContents 列舉
description: 由 IResultsViewer 內容用來指出或設定目前查詢傳回集的顯示方式。
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- ViewContents 列舉舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2070b68ec62a8dd6ca86758b98a6399ee41180eaad24613d17d0825a927b1871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829108"
---
# <a name="viewcontents-enumeration"></a>ViewContents 列舉

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

由 [**IResultsViewer：：內容**](-search-2x-iresultsviewer-contents.md) 用來指出或設定目前查詢傳回集的顯示方式。

## <a name="syntax"></a>Syntax


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**
</dt> <dd>

指出顯示在結果檢視中的內容類型。

</dd> <dt>

<span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**
</dt> <dd>

表示顯示在結果檢視中的內容類型目前設定為 Shell 視圖。

</dd> <dt>

<span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**
</dt> <dd>

表示顯示在結果檢視中的內容類型目前設定為瀏覽器視圖。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>WdsView .idl</dt> </dl> |



 

 





