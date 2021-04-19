---
description: 列出 SSPI API 使用的控制碼。
ms.assetid: 94b622d0-7c04-4513-841f-0df9b5d49136
title: SSPI 控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e388633cfee0d0f0470e519bac124a0bd1c70fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984650"
---
# <a name="sspi-handles"></a><span data-ttu-id="da64b-103">SSPI 控制碼</span><span class="sxs-lookup"><span data-stu-id="da64b-103">SSPI Handles</span></span>

<span data-ttu-id="da64b-104">SSPI 會使用下列控制碼類型以及這些控制碼的指標：</span><span class="sxs-lookup"><span data-stu-id="da64b-104">SSPI uses the following handle types and pointer to these handles:</span></span>

-   <span data-ttu-id="da64b-105">**SecHandle** 和 **PSecHandle**</span><span class="sxs-lookup"><span data-stu-id="da64b-105">**SecHandle** and **PSecHandle**</span></span>
-   <span data-ttu-id="da64b-106">**CredHandle** 和 **PCredHandle**</span><span class="sxs-lookup"><span data-stu-id="da64b-106">**CredHandle** and **PCredHandle**</span></span>
-   <span data-ttu-id="da64b-107">**CtxtHandle** 和 **PCtxtHandle**</span><span class="sxs-lookup"><span data-stu-id="da64b-107">**CtxtHandle** and **PCtxtHandle**</span></span>

<span data-ttu-id="da64b-108">這些控制碼類型的控制碼型別和指標定義如下。</span><span class="sxs-lookup"><span data-stu-id="da64b-108">These handle types and pointers to these handle types are defined as follows.</span></span>


```C++
typedef struct _SecHandle {
  ULONG_PTR       dwLower;
  ULONG_PTR       dwUpper;
} SecHandle, * PSecHandle;

typedef SecHandle    CredHandle;
typedef PSecHandle   PCredHandle;

typedef SecHandle    CtxtHandle;
typedef PSecHandle   PCtxtHandle;
```



 

 



