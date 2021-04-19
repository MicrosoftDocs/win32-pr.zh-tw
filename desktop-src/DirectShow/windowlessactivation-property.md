---
description: WindowlessActivation 屬性會在設計階段為視窗化或無視窗模式初始化 MSWebDVD 物件。
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: WindowlessActivation 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427fdcb265d60200bfe8716cd1ece384861fbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999936"
---
# <a name="windowlessactivation-property"></a>WindowlessActivation 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`WindowlessActivation`屬性會在設計階段為視窗化或無視窗模式初始化 **MSWebDVD** 物件。

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a>傳回值

傳回物件是否為視窗模式的布林值。

## <a name="remarks"></a>備註

此屬性是讀取/寫入，預設值為 true。 因此，如果您在視窗化的容器中執行 **MSWebDVD** 物件，則只需要設定這個屬性。 當包含在 Microsoft® Internet Explorer 的網頁時， **MSWebDVD** 一律會處於無視窗模式，而您不需要設定此屬性。

 

 



