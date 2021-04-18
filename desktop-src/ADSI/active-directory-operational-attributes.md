---
title: Active Directory 操作屬性
description: 操作屬性是目錄中儲存和使用的屬性，供系統管理之用。
ms.assetid: 07453dc0-747e-4b34-946e-1adb90ea532c
ms.tgt_platform: multiple
keywords:
- 屬性 ADSI、操作屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac95536564f735e8e1bd8c5c28a49ce71a2640a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371855"
---
# <a name="active-directory-operational-attributes"></a><span data-ttu-id="584dc-104">Active Directory 操作屬性</span><span class="sxs-lookup"><span data-stu-id="584dc-104">Active Directory Operational Attributes</span></span>

<span data-ttu-id="584dc-105">操作屬性是目錄中儲存和使用的屬性，供系統管理之用。</span><span class="sxs-lookup"><span data-stu-id="584dc-105">Operational attributes are properties that are stored in and used by the directory for administrative purposes.</span></span> <span data-ttu-id="584dc-106">例如，您可能會維護一個操作屬性，以記錄另一個屬性修改時的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="584dc-106">For example, you might maintain an operational attribute to log the date and time when another attribute is modified.</span></span> <span data-ttu-id="584dc-107">您必須使用 [**GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)的呼叫來明確地取出操作屬性。</span><span class="sxs-lookup"><span data-stu-id="584dc-107">Operational Attributes must be explicitly retrieved with a call to [**GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex).</span></span>

 

 




