---
description: 寫入器和要求者都會維護其專屬元資料檔案中的備份或還原作業所需的資訊。
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: VSS 中繼資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e718d3fb0290f8610944180c079e4d615124eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972635"
---
# <a name="vss-metadata"></a><span data-ttu-id="519ce-103">VSS 中繼資料</span><span class="sxs-lookup"><span data-stu-id="519ce-103">VSS Metadata</span></span>

<span data-ttu-id="519ce-104">寫入器和要求者都會維護其專屬元資料檔案中的備份或還原作業所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="519ce-104">Both writers and requesters maintain information necessary to a backup or restore operation in their own metadata documents.</span></span>

<span data-ttu-id="519ce-105">這些檔（分別是 [*寫入器元資料檔案*](vssgloss-w.md) 和 [*備份元件檔*](vssgloss-b.md)）是用來做為寫入器和要求者通訊的基礎，以及備份和還原活動期間的協調。</span><span class="sxs-lookup"><span data-stu-id="519ce-105">These documents, the [*Writer Metadata Document*](vssgloss-w.md) and the [*Backup Components Document*](vssgloss-b.md), respectively, are used as the basis for writer and requester communication and coordination during backup and restore activities.</span></span>

<span data-ttu-id="519ce-106">中繼資料是使用專屬架構以 XML 格式表示。</span><span class="sxs-lookup"><span data-stu-id="519ce-106">The metadata is represented in XML format using a proprietary schema.</span></span> <span data-ttu-id="519ce-107">中繼資料可以複製到磁片、磁帶或任何其他的大型存放裝置。</span><span class="sxs-lookup"><span data-stu-id="519ce-107">Metadata can be copied to disk, tape, or any other mass storage device.</span></span> <span data-ttu-id="519ce-108">在備份作業期間，應該一律將其儲存至備份媒體，而且必須在還原作業期間從該媒體中取出。</span><span class="sxs-lookup"><span data-stu-id="519ce-108">It should always be saved to the backup media during a backup operation, and will need to be retrieved from that media in the course of a restore operation.</span></span>

<span data-ttu-id="519ce-109">**注意：** 格式和架構的特定詳細資料僅供系統使用。</span><span class="sxs-lookup"><span data-stu-id="519ce-109">**Caution:** The specific details of the format and schema are for system use only.</span></span> <span data-ttu-id="519ce-110">開發人員不應該嘗試修改或直接使用中繼資料的 XML 表示。</span><span class="sxs-lookup"><span data-stu-id="519ce-110">Developers should not attempt to modify or directly use the XML representation of the metadata.</span></span>

<span data-ttu-id="519ce-111">撰寫者和要求者可透過各種查詢來提供，並設定方法來存取和修改備份元件和寫入器元資料檔案：</span><span class="sxs-lookup"><span data-stu-id="519ce-111">Writers and requesters are provided with a variety of query and set methods to access and modify the Backup Components and Writer Metadata documents:</span></span>

-   [<span data-ttu-id="519ce-112">使用寫入器元資料檔案</span><span class="sxs-lookup"><span data-stu-id="519ce-112">Working with the Writer Metadata Document</span></span>](working-with-the-writer-metadata-document.md)
-   [<span data-ttu-id="519ce-113">使用備份元件檔</span><span class="sxs-lookup"><span data-stu-id="519ce-113">Working with the Backup Components Document</span></span>](working-with-the-backup-components-document.md)
-   [<span data-ttu-id="519ce-114">VSS 中繼資料元件</span><span class="sxs-lookup"><span data-stu-id="519ce-114">VSS Metadata Components</span></span>](vss-metadata-components.md)

 

 



