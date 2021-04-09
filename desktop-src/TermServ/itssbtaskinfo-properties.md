---
title: ITsSbTaskInfo 屬性
description: ITsSbTaskInfo 介面會公開下列屬性。
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e4c8fefc2e443778b2ce177e61a314a3e0ef9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678388"
---
# <a name="itssbtaskinfo-properties"></a><span data-ttu-id="5bd24-103">ITsSbTaskInfo 屬性</span><span class="sxs-lookup"><span data-stu-id="5bd24-103">ITsSbTaskInfo Properties</span></span>

<span data-ttu-id="5bd24-104">[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)介面會公開下列屬性。</span><span class="sxs-lookup"><span data-stu-id="5bd24-104">The [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5bd24-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="5bd24-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="5bd24-106">**CoNtext 屬性**</span><span class="sxs-lookup"><span data-stu-id="5bd24-106">**Context property**</span></span>](itssbtaskinfo-context.md)
</dt> <dd>

<span data-ttu-id="5bd24-107">捕獲與工作相關聯的內容位元組。</span><span class="sxs-lookup"><span data-stu-id="5bd24-107">Retrieves the context bytes associated with the task.</span></span>

</dd> <dt>

[<span data-ttu-id="5bd24-108">**期限屬性**</span><span class="sxs-lookup"><span data-stu-id="5bd24-108">**Deadline property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

<span data-ttu-id="5bd24-109">抓取必須起始工作的時間。</span><span class="sxs-lookup"><span data-stu-id="5bd24-109">Retrieves the time by which the task must be initiated.</span></span> <span data-ttu-id="5bd24-110">這是用來排列修補程式的優先順序。</span><span class="sxs-lookup"><span data-stu-id="5bd24-110">This is used to prioritize patches.</span></span> <span data-ttu-id="5bd24-111">系統會先起始最早期限的修補程式。</span><span class="sxs-lookup"><span data-stu-id="5bd24-111">The patch with the earliest deadline will get initiated first.</span></span>

</dd> <dt>

[<span data-ttu-id="5bd24-112">**EndTime 屬性**</span><span class="sxs-lookup"><span data-stu-id="5bd24-112">**EndTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

<span data-ttu-id="5bd24-113">抓取工作代理程式可以啟動工作的最晚時間。</span><span class="sxs-lookup"><span data-stu-id="5bd24-113">Retrieves the latest time the task agent can start the task.</span></span>

</dd> <dt>

<span data-ttu-id="5bd24-114">[**[識別項] 屬性**](itssbtaskinfo-identifier.md)</span><span class="sxs-lookup"><span data-stu-id="5bd24-114">[**Identifier property**](itssbtaskinfo-identifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="5bd24-115">抓取由工作代理程式當做唯一識別碼使用的 GUID。</span><span class="sxs-lookup"><span data-stu-id="5bd24-115">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="5bd24-116">**標籤屬性**</span><span class="sxs-lookup"><span data-stu-id="5bd24-116">**Label property**</span></span>](itssbtaskinfo-label.md)
</dt> <dd>

<span data-ttu-id="5bd24-117">抓取描述工作用途的標籤。</span><span class="sxs-lookup"><span data-stu-id="5bd24-117">Retrieves the label that describes the purpose of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="5bd24-118">**外掛程式屬性**</span><span class="sxs-lookup"><span data-stu-id="5bd24-118">**Plugin property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

<span data-ttu-id="5bd24-119">抓取工作代理程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5bd24-119">Retrieves the display name of the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="5bd24-120">**StartTime 屬性**</span><span class="sxs-lookup"><span data-stu-id="5bd24-120">**StartTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

<span data-ttu-id="5bd24-121">抓取工作代理程式可以啟動工作的最早時間。</span><span class="sxs-lookup"><span data-stu-id="5bd24-121">Retrieves the earliest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="5bd24-122">**Status 屬性**</span><span class="sxs-lookup"><span data-stu-id="5bd24-122">**Status property**</span></span>](itssbtaskinfo-status.md)
</dt> <dd>

<span data-ttu-id="5bd24-123">抓取 [**RDV 工作 \_ \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) 列舉值，這個值表示工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="5bd24-123">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="5bd24-124">**TargetId 屬性**</span><span class="sxs-lookup"><span data-stu-id="5bd24-124">**TargetId property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

<span data-ttu-id="5bd24-125">抓取目標識別碼。</span><span class="sxs-lookup"><span data-stu-id="5bd24-125">Retrieves the target identifier.</span></span>

</dd> </dl>

 

 




