---
title: ISearchDesktop ExecuteSQLQuery 方法
description: 取得包含結構化查詢語言 (SQL)  (SQL) 查詢及其屬性的字串指標，並將指標傳回給傳回集。
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- ExecuteSQLQuery 方法舊版 Windows 環境功能
- ExecuteSQLQuery 方法舊版 Windows 環境功能，ISearchDesktop 介面
- ISearchDesktop 介面舊版 Windows 環境功能，ExecuteSQLQuery 方法
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0b13ff361d07f99efe1366e2201d610eac10523
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2020
ms.locfileid: "103681535"
---
# <a name="isearchdesktopexecutesqlquery-method"></a><span data-ttu-id="d9ea7-106">ISearchDesktop：： ExecuteSQLQuery 方法</span><span class="sxs-lookup"><span data-stu-id="d9ea7-106">ISearchDesktop::ExecuteSQLQuery method</span></span>

> [!NOTE]
> <span data-ttu-id="d9ea7-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="d9ea7-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d9ea7-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="d9ea7-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d9ea7-109">取得包含結構化查詢語言 (SQL)  (SQL) 查詢及其屬性的字串指標，並將指標傳回給傳回集。</span><span class="sxs-lookup"><span data-stu-id="d9ea7-109">Takes a pointer to a string that contains a Structured Query Language (SQL) query and its attributes and returns a pointer to the return set.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9ea7-110">語法</span><span class="sxs-lookup"><span data-stu-id="d9ea7-110">Syntax</span></span>


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a><span data-ttu-id="d9ea7-111">參數</span><span class="sxs-lookup"><span data-stu-id="d9ea7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9ea7-112">*pdwAttributes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9ea7-112">*pdwAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9ea7-113">類型： **LPCWSTR \***</span><span class="sxs-lookup"><span data-stu-id="d9ea7-113">Type: **LPCWSTR\***</span></span>

<span data-ttu-id="d9ea7-114">字串，包含查詢的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="d9ea7-114">A string that contains the other attributes for the query.</span></span>

</dd> <dt>

<span data-ttu-id="d9ea7-115">*pwszURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9ea7-115">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9ea7-116">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="d9ea7-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="d9ea7-117">包含 SQL 查詢的字串。</span><span class="sxs-lookup"><span data-stu-id="d9ea7-117">A string that contains the SQL query.</span></span>

</dd> <dt>

<span data-ttu-id="d9ea7-118">*ppidUrl* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d9ea7-118">*ppidUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9ea7-119">類型： **ppidUrl \***</span><span class="sxs-lookup"><span data-stu-id="d9ea7-119">Type: **ppidUrl\***</span></span>

<span data-ttu-id="d9ea7-120">當這個方法成功傳回時，會包含傳回之記錄集的指標。</span><span class="sxs-lookup"><span data-stu-id="d9ea7-120">When this method returns successfully, contains a pointer to the returned recordset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9ea7-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9ea7-121">Return value</span></span>

<span data-ttu-id="d9ea7-122">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d9ea7-122">Type: **HRESULT**</span></span>

<span data-ttu-id="d9ea7-123">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d9ea7-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d9ea7-124">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d9ea7-124">Otherwise, it returns an **HRESULT** error code.</span></span>

 

 




