---
title: IDODownloadInternal 介面
description: 用來取得或設定擴充的下載屬性。
keywords:
- IDODownloadInternal 介面
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092975"
---
# <a name="idodownloadinternal-interface"></a><span data-ttu-id="988ec-104">IDODownloadInternal 介面</span><span class="sxs-lookup"><span data-stu-id="988ec-104">IDODownloadInternal interface</span></span>

> [!IMPORTANT]
> <span data-ttu-id="988ec-105">**IDODownloadInternal** 介面已被取代。</span><span class="sxs-lookup"><span data-stu-id="988ec-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="988ec-106">請改用 [IDODownload](../do/nn-do-idodownload.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="988ec-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="988ec-107">**IDODownloadInternal** 介面可用來取得或設定擴充的下載屬性。</span><span class="sxs-lookup"><span data-stu-id="988ec-107">The **IDODownloadInternal** interface is used to get or set extended download properties.</span></span>

## <a name="methods"></a><span data-ttu-id="988ec-108">方法</span><span class="sxs-lookup"><span data-stu-id="988ec-108">Methods</span></span>

<span data-ttu-id="988ec-109">**IDODownloadInternal** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="988ec-109">The **IDODownloadInternal** interface has these methods.</span></span>

| <span data-ttu-id="988ec-110">方法</span><span class="sxs-lookup"><span data-stu-id="988ec-110">Method</span></span> | <span data-ttu-id="988ec-111">描述</span><span class="sxs-lookup"><span data-stu-id="988ec-111">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="988ec-112">IDODownloadInternal::GetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="988ec-112">IDODownloadInternal::GetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | <span data-ttu-id="988ec-113">抓取包含特定延伸下載屬性值之 **變數** 的指標。</span><span class="sxs-lookup"><span data-stu-id="988ec-113">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span> |
| [<span data-ttu-id="988ec-114">IDODownloadInternal::SetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="988ec-114">IDODownloadInternal::SetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | <span data-ttu-id="988ec-115">設定延伸的下載屬性。</span><span class="sxs-lookup"><span data-stu-id="988ec-115">Sets an extended download property.</span></span> <span data-ttu-id="988ec-116">方法會接受 **VARIANT** 的指標，其中包含要套用至下載的特定屬性值。</span><span class="sxs-lookup"><span data-stu-id="988ec-116">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="988ec-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="988ec-117">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="988ec-118">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="988ec-118">**Minimum supported client**</span></span> | <span data-ttu-id="988ec-119">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="988ec-119">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="988ec-120">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="988ec-120">**Minimum supported server**</span></span> | <span data-ttu-id="988ec-121">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="988ec-121">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="988ec-122">**標頭**</span><span class="sxs-lookup"><span data-stu-id="988ec-122">**Header**</span></span> | <span data-ttu-id="988ec-123">DODownloadInternal。h</span><span class="sxs-lookup"><span data-stu-id="988ec-123">DODownloadInternal.h</span></span> |