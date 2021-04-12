---
description: 封裝作者應確定任何自訂資料表、屬性或其封裝中所定義之動作的名稱，都不會與標準資料表、屬性或 Windows Installer 的原生名稱相衝突。
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: 命名自訂資料表、屬性和動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848773"
---
# <a name="naming-custom-tables-properties-and-actions"></a><span data-ttu-id="35890-103">命名自訂資料表、屬性和動作</span><span class="sxs-lookup"><span data-stu-id="35890-103">Naming Custom Tables, Properties, and Actions</span></span>

<span data-ttu-id="35890-104">封裝作者應確定任何自訂資料表、屬性或其封裝中所定義之動作的名稱，都不會與標準資料表、屬性或 Windows Installer 的原生名稱相衝突。</span><span class="sxs-lookup"><span data-stu-id="35890-104">Package authors should ensure that the names of any custom tables, properties, or actions defined in their package will not conflict with the names of standard tables, properties, or actions that are native to the Windows Installer.</span></span>

<span data-ttu-id="35890-105">封裝作者應遵守自訂資料表、屬性或動作名稱的下列指導方針。</span><span class="sxs-lookup"><span data-stu-id="35890-105">Package authors should adhere to the following guidelines for custom table, property, or action names.</span></span>

-   <span data-ttu-id="35890-106">為具有前置詞的自訂資料表、屬性或動作建立名稱，以識別您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="35890-106">Make names for custom tables, properties, or actions that have a prefix that identifies your application.</span></span>
-   <span data-ttu-id="35890-107">請勿使用 Msi 的名稱作為前置詞。</span><span class="sxs-lookup"><span data-stu-id="35890-107">Never use a name with Msi as the prefix.</span></span> <span data-ttu-id="35890-108">從 Windows Installer 2.0 開始，所有新的原生 Windows Installer 屬性、動作和資料表都會命名為 Msi 的前置詞。</span><span class="sxs-lookup"><span data-stu-id="35890-108">Starting with Windows Installer 2.0, all new native Windows Installer properties, actions, and tables are given names prefixed by Msi.</span></span> <span data-ttu-id="35890-109">這個前置詞不區分大小寫，例如 MsiNewInternalTable。</span><span class="sxs-lookup"><span data-stu-id="35890-109">This prefix is not case sensitive, for example MsiNewInternalTable.</span></span> <span data-ttu-id="35890-110">因為前置詞不區分大小寫，所以作者應避免 Msi 前置詞的所有案例。</span><span class="sxs-lookup"><span data-stu-id="35890-110">Because the prefix is not case sensitive, authors should avoid all cases of the Msi prefix.</span></span>

<span data-ttu-id="35890-111">如需詳細資訊，請參閱 [資料表名稱](table-names.md)。</span><span class="sxs-lookup"><span data-stu-id="35890-111">For more information, see [Table Names](table-names.md).</span></span>

 

 



