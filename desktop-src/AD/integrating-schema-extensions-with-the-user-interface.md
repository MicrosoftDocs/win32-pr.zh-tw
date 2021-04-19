---
title: 整合架構延伸與消費者介面
description: Active Directory Domain Services 的管理工具使用通用的架構，將系統管理使用者介面連接到目錄架構。
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446c3b5150d66357206bd1eb139a391d2408ee9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968412"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a><span data-ttu-id="211e2-103">整合架構延伸與消費者介面</span><span class="sxs-lookup"><span data-stu-id="211e2-103">Integrating Schema Extensions with the User Interface</span></span>

<span data-ttu-id="211e2-104">Active Directory Domain Services 的管理工具使用通用的架構，將系統管理使用者介面連接到目錄架構。</span><span class="sxs-lookup"><span data-stu-id="211e2-104">The administration tools of Active Directory Domain Services use a common architecture for connecting the administrative user interface to the directory schema.</span></span> <span data-ttu-id="211e2-105">此架構的文字核心是 **displaySpecifier** 物件類別。</span><span class="sxs-lookup"><span data-stu-id="211e2-105">The centerpiece of this architecture is the **displaySpecifier** object class.</span></span> <span data-ttu-id="211e2-106">在 [擴充目錄物件的消費者介面](extending-the-user-interface-for-directory-objects.md)時，會詳細說明顯示規範及其用法。</span><span class="sxs-lookup"><span data-stu-id="211e2-106">Display specifiers and their usage are described in detail in [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

<span data-ttu-id="211e2-107">當您藉由子類別化現有類別來建立新類別時，您可以藉由複製超級類別的顯示規範來利用超類別的現有 UI。</span><span class="sxs-lookup"><span data-stu-id="211e2-107">When you create a new class by subclassing an existing class, you can leverage the existing UI for the superclass by copying the superclass' display specifier.</span></span> <span data-ttu-id="211e2-108">複製類別的顯示規範的簡單方式，就是使用 LDIFDE 將它匯出至 LDIF 檔案、編輯辨別名稱和 CN，然後匯入修改過的 LDIF 檔案。</span><span class="sxs-lookup"><span data-stu-id="211e2-108">An easy way to copy the display specifier for a class is to export it into an LDIF file using LDIFDE, edit the Distinguished name and CN, then import the modified LDIF file.</span></span> <span data-ttu-id="211e2-109">如果子類別具有其他屬性，您將需要提供額外的屬性頁來支援編輯。</span><span class="sxs-lookup"><span data-stu-id="211e2-109">If the subclass has additional attributes, you will need to provide additional property pages to support editing.</span></span> <span data-ttu-id="211e2-110">如果子類別具有其他的必須具有屬性，您就必須提供建立對話方塊延伸頁面，因為超級類別提供的 UI 無法建立這些新屬性。</span><span class="sxs-lookup"><span data-stu-id="211e2-110">If the subclass has additional must-have properties, you will need to provide Creation Dialog extension pages since the UI provided by the superclass has no way to create these new attributes.</span></span>

 

 




