---
title: IDOManager 介面
description: 用來建立新的下載，以及列舉現有的下載。
keywords:
- IDOManager 介面
topic_type:
- apiref
api_name:
- IDOManager
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a8755615e4d2f0fd074117438f8f305dce0cb681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106996372"
---
# <a name="idomanager-interface"></a><span data-ttu-id="41067-104">IDOManager 介面</span><span class="sxs-lookup"><span data-stu-id="41067-104">IDOManager interface</span></span>

<span data-ttu-id="41067-105">**IDOManager** 介面可用來建立新的下載，以及列舉現有的下載。</span><span class="sxs-lookup"><span data-stu-id="41067-105">The **IDOManager** interface is used to create a new download, and to enumerate existing downloads.</span></span>

## <a name="methods"></a><span data-ttu-id="41067-106">方法</span><span class="sxs-lookup"><span data-stu-id="41067-106">Methods</span></span>

<span data-ttu-id="41067-107">**IDOManager** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="41067-107">The **IDOManager** interface has these methods.</span></span>

| <span data-ttu-id="41067-108">方法</span><span class="sxs-lookup"><span data-stu-id="41067-108">Method</span></span> | <span data-ttu-id="41067-109">描述</span><span class="sxs-lookup"><span data-stu-id="41067-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="41067-110">IDOManager::CreateDownload</span><span class="sxs-lookup"><span data-stu-id="41067-110">IDOManager::CreateDownload</span></span>](./nf-do-idomanager-createdownload.md) | <span data-ttu-id="41067-111">建立新的下載。</span><span class="sxs-lookup"><span data-stu-id="41067-111">Creates a new download.</span></span> |
| [<span data-ttu-id="41067-112">IDOManager::EnumDownloads</span><span class="sxs-lookup"><span data-stu-id="41067-112">IDOManager::EnumDownloads</span></span>](./nf-do-idomanager-enumdownloads.md) | <span data-ttu-id="41067-113">抓取列舉值物件的介面指標，此列舉值物件是用來列舉現有的下載。</span><span class="sxs-lookup"><span data-stu-id="41067-113">Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.</span></span> |

## <a name="requirements"></a><span data-ttu-id="41067-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="41067-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="41067-115">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="41067-115">**Minimum supported client**</span></span> | <span data-ttu-id="41067-116">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41067-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="41067-117">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="41067-117">**Minimum supported server**</span></span> | <span data-ttu-id="41067-118">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41067-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="41067-119">**標頭**</span><span class="sxs-lookup"><span data-stu-id="41067-119">**Header**</span></span> | <span data-ttu-id="41067-120">Do。h</span><span class="sxs-lookup"><span data-stu-id="41067-120">Do.h</span></span> |