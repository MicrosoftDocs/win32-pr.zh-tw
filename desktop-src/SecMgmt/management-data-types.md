---
description: 列出安全性設定附件 Dll 及其支援函數所使用的資料類型。
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: 安全性管理資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998504"
---
# <a name="security-management-data-types"></a><span data-ttu-id="206e2-103">安全性管理資料類型</span><span class="sxs-lookup"><span data-stu-id="206e2-103">Security Management Data Types</span></span>

<span data-ttu-id="206e2-104">安全性管理資料類型包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="206e2-104">The security management data types include the following:</span></span>

-   [<span data-ttu-id="206e2-105">附件資料類型</span><span class="sxs-lookup"><span data-stu-id="206e2-105">Attachment Data Types</span></span>](#attachment-data-types)
-   [<span data-ttu-id="206e2-106">LSA 原則資料類型</span><span class="sxs-lookup"><span data-stu-id="206e2-106">LSA Policy Data Types</span></span>](#lsa-policy-data-types)

## <a name="attachment-data-types"></a><span data-ttu-id="206e2-107">附件資料類型</span><span class="sxs-lookup"><span data-stu-id="206e2-107">Attachment Data Types</span></span>

<span data-ttu-id="206e2-108">安全性設定附件 Dll 和其支援的函式會使用下列資料類型。</span><span class="sxs-lookup"><span data-stu-id="206e2-108">The following data types are used by the Security Configuration attachment DLLs and their supporting functions.</span></span>



| <span data-ttu-id="206e2-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="206e2-109">Data type</span></span>                                                    | <span data-ttu-id="206e2-110">描述</span><span class="sxs-lookup"><span data-stu-id="206e2-110">Description</span></span>                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="206e2-111">**SCE \_ 列舉 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="206e2-111">**SCE\_ENUMERATION\_CONTEXT**</span></span>](sce-enumeration-context.md) | <span data-ttu-id="206e2-112">供 [**PFSCE \_ 查詢 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) 函數用來流覽安全性資料庫。</span><span class="sxs-lookup"><span data-stu-id="206e2-112">Used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>                                                                                                                                              |
| [<span data-ttu-id="206e2-113">**SCE \_ 把手**</span><span class="sxs-lookup"><span data-stu-id="206e2-113">**SCE\_HANDLE**</span></span>](sce-handle.md)                            | <span data-ttu-id="206e2-114">用來 [**PFSCE \_ 查詢 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) 和 [**PFSCE \_ 設定 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) ，以便在附件和安全性資料庫之間傳遞資訊。</span><span class="sxs-lookup"><span data-stu-id="206e2-114">Used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to pass information between the attachment and the security database.</span></span>                                                                                 |
| [<span data-ttu-id="206e2-115">**SCESTATUS**</span><span class="sxs-lookup"><span data-stu-id="206e2-115">**SCESTATUS**</span></span>](scestatus.md)                               | <span data-ttu-id="206e2-116">「安全性設定工具集 API」會使用資料類型來傳回函式呼叫結果的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="206e2-116">Data type is used by the Security Configuration tool set API to return information about the results of a function call.</span></span>                                                                                                                                    |
| [<span data-ttu-id="206e2-117">**SCESVC \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="206e2-117">**SCESVC\_HANDLE**</span></span>](scesvc-handle.md)                      | <span data-ttu-id="206e2-118">由 [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) 和 [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) 介面的方法所使用，可在 [安全性設定] 嵌入式管理單元和嵌入式管理單元擴充功能之間傳遞資訊。</span><span class="sxs-lookup"><span data-stu-id="206e2-118">Used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span> |
| [<span data-ttu-id="206e2-119">**SCESVC \_ 資訊 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="206e2-119">**SCESVC\_INFO\_TYPE**</span></span>](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | <span data-ttu-id="206e2-120">列舉是用來 [**PFSCE \_ 查詢 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) 和 [**PFSCE \_ 設定 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) ，以指出向安全性資料庫要求或傳遞的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="206e2-120">Enumeration is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to indicate the type of information requested from or passed to the security database.</span></span>                                                 |



 

## <a name="lsa-policy-data-types"></a><span data-ttu-id="206e2-121">LSA 原則資料類型</span><span class="sxs-lookup"><span data-stu-id="206e2-121">LSA Policy Data Types</span></span>

<span data-ttu-id="206e2-122">LSA 原則管理函數會使用下列資料類型。</span><span class="sxs-lookup"><span data-stu-id="206e2-122">The following data types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="206e2-123">資料類型</span><span class="sxs-lookup"><span data-stu-id="206e2-123">Data type</span></span>                                                  | <span data-ttu-id="206e2-124">描述</span><span class="sxs-lookup"><span data-stu-id="206e2-124">Description</span></span>                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="206e2-125">**LSA \_ 列舉 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="206e2-125">**LSA\_ENUMERATION\_HANDLE**</span></span>](lsa-enumeration-handle.md) | <span data-ttu-id="206e2-126">用來追蹤需要多個函式呼叫的列舉。</span><span class="sxs-lookup"><span data-stu-id="206e2-126">Used to track enumerations in which multiple function calls are required.</span></span> |
| [<span data-ttu-id="206e2-127">**LSA \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="206e2-127">**LSA\_HANDLE**</span></span>](lsa-handle.md)                          | <span data-ttu-id="206e2-128">[**原則**](policy-object.md)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="206e2-128">Handle to a [**Policy**](policy-object.md) object.</span></span>                       |



 

 

 
