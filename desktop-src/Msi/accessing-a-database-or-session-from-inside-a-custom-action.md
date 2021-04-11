---
description: 您無法從非目前安裝會話的自訂動作存取安裝程式會話。
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: 從自訂動作內部存取資料庫或會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944053"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a><span data-ttu-id="038a3-103">從自訂動作內部存取資料庫或會話</span><span class="sxs-lookup"><span data-stu-id="038a3-103">Accessing a Database or Session from Inside a Custom Action</span></span>

<span data-ttu-id="038a3-104">您無法從非目前安裝會話的自訂動作存取安裝程式會話。</span><span class="sxs-lookup"><span data-stu-id="038a3-104">You cannot access an installer session from a custom action that is not the current installation session.</span></span> <span data-ttu-id="038a3-105">自訂動作僅限使用會話的使用中資料庫，而且沒有其他資料庫。</span><span class="sxs-lookup"><span data-stu-id="038a3-105">Custom actions are limited to working with only the active database of the session and no other databases.</span></span> <span data-ttu-id="038a3-106">下列 Windows Installer [資料庫函數](database-functions.md) 不能從自訂動作呼叫，因為它們需要資料庫的控制碼，而不是目前安裝會話的資料庫：</span><span class="sxs-lookup"><span data-stu-id="038a3-106">The following Windows Installer [Database Functions](database-functions.md) must not be called from a custom action, because they require a handle to a database that is not the database of the current installation session:</span></span>

[<span data-ttu-id="038a3-107">**MsiDatabaseMerge**</span><span class="sxs-lookup"><span data-stu-id="038a3-107">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[<span data-ttu-id="038a3-108">**MsiCreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="038a3-108">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[<span data-ttu-id="038a3-109">**MsiDatabaseApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="038a3-109">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[<span data-ttu-id="038a3-110">**MsiDatabaseCommit**</span><span class="sxs-lookup"><span data-stu-id="038a3-110">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[<span data-ttu-id="038a3-111">**MsiDatabaseExport**</span><span class="sxs-lookup"><span data-stu-id="038a3-111">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[<span data-ttu-id="038a3-112">**MsiDatabaseGenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="038a3-112">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[<span data-ttu-id="038a3-113">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="038a3-113">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[<span data-ttu-id="038a3-114">**MsiEnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="038a3-114">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[<span data-ttu-id="038a3-115">**MsiGetDatabaseState**</span><span class="sxs-lookup"><span data-stu-id="038a3-115">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a><span data-ttu-id="038a3-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="038a3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="038a3-117">從自訂動作內部存取目前的安裝程式會話</span><span class="sxs-lookup"><span data-stu-id="038a3-117">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



