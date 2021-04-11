---
description: 在 Windows Search 索引子中建立新的自訂目錄，並傳回它的參考。
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: ISearchManager2：： Start-createcatalog 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 009e34a2d1eb4d18df1747ba01ea39c3360ec81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191194"
---
# <a name="isearchmanager2createcatalog-method"></a><span data-ttu-id="26ea4-103">ISearchManager2：： Start-createcatalog 方法</span><span class="sxs-lookup"><span data-stu-id="26ea4-103">ISearchManager2::CreateCatalog method</span></span>

<span data-ttu-id="26ea4-104">在 Windows Search 索引子中建立新的自訂目錄，並傳回它的參考。</span><span class="sxs-lookup"><span data-stu-id="26ea4-104">Creates a new custom catalog in the Windows Search indexer and returns a reference to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ea4-105">語法</span><span class="sxs-lookup"><span data-stu-id="26ea4-105">Syntax</span></span>


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a><span data-ttu-id="26ea4-106">參數</span><span class="sxs-lookup"><span data-stu-id="26ea4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26ea4-107">*pszCatalog* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26ea4-107">*pszCatalog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26ea4-108">類型： **[ **LPCWSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26ea4-108">Type: **[**LPCWSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26ea4-109">要建立的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="26ea4-109">Name of catalog to create.</span></span> <span data-ttu-id="26ea4-110">可以是呼叫者所選取的任何名稱，必須只包含標準的英數位元和底線。</span><span class="sxs-lookup"><span data-stu-id="26ea4-110">Can be any name selected by the caller, must contain only standard alphanumeric characters and underscore.</span></span>

</dd> <dt>

<span data-ttu-id="26ea4-111">*ppCatalogManager* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="26ea4-111">*ppCatalogManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26ea4-112">類型： **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span><span class="sxs-lookup"><span data-stu-id="26ea4-112">Type: **[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span></span>

<span data-ttu-id="26ea4-113">成功時，會以 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 介面指標的形式傳回所建立目錄的參考。</span><span class="sxs-lookup"><span data-stu-id="26ea4-113">On success a reference to the created catalog is returned as an [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) interface pointer.</span></span> <span data-ttu-id="26ea4-114">在呼叫的應用程式完成使用之後，必須在此介面上呼叫 Release () 。</span><span class="sxs-lookup"><span data-stu-id="26ea4-114">The Release() must be called on this interface after the calling application has finished using it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26ea4-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="26ea4-115">Return value</span></span>

<span data-ttu-id="26ea4-116">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="26ea4-116">Type: **HRESULT**</span></span>

<span data-ttu-id="26ea4-117">HRESULT，指出作業的狀態：</span><span class="sxs-lookup"><span data-stu-id="26ea4-117">HRESULT indicating status of operation:</span></span>



| <span data-ttu-id="26ea4-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="26ea4-118">Return code</span></span>                                                                             | <span data-ttu-id="26ea4-119">Description</span><span class="sxs-lookup"><span data-stu-id="26ea4-119">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="26ea4-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="26ea4-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="26ea4-121">目錄先前未存在且已建立。</span><span class="sxs-lookup"><span data-stu-id="26ea4-121">Catalog did not previously exist and was created.</span></span> <span data-ttu-id="26ea4-122">傳回的目錄參考。</span><span class="sxs-lookup"><span data-stu-id="26ea4-122">Reference to catalog returned.</span></span><br/> |
| <dl> <span data-ttu-id="26ea4-123"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="26ea4-123"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="26ea4-124">目錄先前已存在，參考至所傳回的目錄。</span><span class="sxs-lookup"><span data-stu-id="26ea4-124">Catalog previously existed, reference to catalog returned.</span></span><br/>                       |



 

<span data-ttu-id="26ea4-125">失敗的 HRESULT：無法建立目錄或傳遞的引數無效。</span><span class="sxs-lookup"><span data-stu-id="26ea4-125">FAILED HRESULT: Failure creating catalog or invalid arguments passed.</span></span>

## <a name="remarks"></a><span data-ttu-id="26ea4-126">備註</span><span class="sxs-lookup"><span data-stu-id="26ea4-126">Remarks</span></span>

<span data-ttu-id="26ea4-127">呼叫以在 Windows Search 索引子中建立新的目錄。</span><span class="sxs-lookup"><span data-stu-id="26ea4-127">Called to create a new catalog in the Windows Search indexer.</span></span> <span data-ttu-id="26ea4-128">建立之後，傳回的 [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 管理員上的方法可以用來新增要編制索引的位置、監視索引編制程式，以及建立要傳送至索引子的查詢並取得結果。</span><span class="sxs-lookup"><span data-stu-id="26ea4-128">After creation, the methods on the returned [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) manager can be used to add locations to be indexed, monitor indexing process, and construct queries to send to the indexer and get results.</span></span> <span data-ttu-id="26ea4-129">如需詳細資訊，請參閱「管理索引」檔： https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="26ea4-129">See the “Managing the Index” documentation for more info: https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span></span>

## <a name="requirements"></a><span data-ttu-id="26ea4-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="26ea4-130">Requirements</span></span>



| <span data-ttu-id="26ea4-131">需求</span><span class="sxs-lookup"><span data-stu-id="26ea4-131">Requirement</span></span> | <span data-ttu-id="26ea4-132">值</span><span class="sxs-lookup"><span data-stu-id="26ea4-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="26ea4-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26ea4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="26ea4-134">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26ea4-134">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="26ea4-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26ea4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="26ea4-136">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26ea4-136">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26ea4-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26ea4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ea4-138">**ISearchManager2**</span><span class="sxs-lookup"><span data-stu-id="26ea4-138">**ISearchManager2**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
