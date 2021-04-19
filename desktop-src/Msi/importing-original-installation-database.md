---
description: 藉由複製原始產品的安裝套件和來原始目錄樹狀結構，開始撰寫升級套件。
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: 匯入原始安裝資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983770"
---
# <a name="importing-original-installation-database"></a><span data-ttu-id="c5509-103">匯入原始安裝資料庫</span><span class="sxs-lookup"><span data-stu-id="c5509-103">Importing Original Installation Database</span></span>

<span data-ttu-id="c5509-104">藉由複製原始產品的安裝套件和來原始目錄樹狀結構，開始撰寫升級套件。</span><span class="sxs-lookup"><span data-stu-id="c5509-104">Begin authoring the upgrade package by copying the installation package and source directory tree of the of original product.</span></span> <span data-ttu-id="c5509-105">[安裝範例](an-installation-example.md)提供撰寫 MNP2000 安裝套件的指示。</span><span class="sxs-lookup"><span data-stu-id="c5509-105">Instructions for authoring the installation package for MNP2000 are given in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="c5509-106">您應該複製下列資料夾的內容：</span><span class="sxs-lookup"><span data-stu-id="c5509-106">You should copy the contents of the following folders:</span></span>

<span data-ttu-id="c5509-107">C： \\ 範例 \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="c5509-107">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="c5509-108">C： \\ 範例 \\ 記事本</span><span class="sxs-lookup"><span data-stu-id="c5509-108">C:\\Sample\\Notepad</span></span>\\

<span data-ttu-id="c5509-109">C： \\ 範例 \\ 二進位檔</span><span class="sxs-lookup"><span data-stu-id="c5509-109">C:\\Sample\\Binary</span></span>\\

<span data-ttu-id="c5509-110">C： \\ 範例 \\ 圖示</span><span class="sxs-lookup"><span data-stu-id="c5509-110">C:\\Sample\\Icon</span></span>\\

<span data-ttu-id="c5509-111">更新 [記事本] 資料夾的內容，使其符合 [規劃主要升級](planning-a-major-upgrade.md)中所述的來源。</span><span class="sxs-lookup"><span data-stu-id="c5509-111">Update the contents of the Notepad folder so that they match the source described in [Planning a Major Upgrade](planning-a-major-upgrade.md).</span></span> <span data-ttu-id="c5509-112">移除所有過時的原始檔（例如 Baseball.txt），並取代為更新的檔案，例如 Baseba01.txt。</span><span class="sxs-lookup"><span data-stu-id="c5509-112">Remove all obsolete source files, such as Baseball.txt, and replace with the updated files, such as Baseba01.txt.</span></span> <span data-ttu-id="c5509-113">新增升級所提供的其他新檔案，例如 Opera01.txt。</span><span class="sxs-lookup"><span data-stu-id="c5509-113">Add the additional new files provided by the upgrade, such as Opera01.txt.</span></span>

<span data-ttu-id="c5509-114">將 MNP2000.msi 重新命名為 MNP2001.msi。</span><span class="sxs-lookup"><span data-stu-id="c5509-114">Rename MNP2000.msi to MNP2001.msi.</span></span> <span data-ttu-id="c5509-115">在後續步驟中，您將使用資料表編輯器，將此資料庫修改為 .msi 檔案以進行升級。</span><span class="sxs-lookup"><span data-stu-id="c5509-115">In subsequent steps you will use a table editor to modify this database into the .msi file for the upgrade.</span></span> <span data-ttu-id="c5509-116">未在後續章節中明確修改的資料庫資料表，與原始產品資料庫中的資料表相同，MNP2000.msi。</span><span class="sxs-lookup"><span data-stu-id="c5509-116">Database tables that are not explicitly modified in the subsequent sections are identical to the tables in the original product's database, MNP2000.msi.</span></span>

[<span data-ttu-id="c5509-117">繼續</span><span class="sxs-lookup"><span data-stu-id="c5509-117">Continue</span></span>](updating-directory-structure-for-an-upgrade.md)

 

 



