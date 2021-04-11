---
description: RemoveMetadataByName 方法的 Proxy 函式。
ms.assetid: fb86766e-234d-4e39-9d4b-7814d50a3867
title: IWICMetadataQueryWriter_RemoveMetadataByName_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_RemoveMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e4681d3fbb93f176129ce2527356306d4ea02fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850415"
---
# <a name="iwicmetadataquerywriter_removemetadatabyname_proxy-function"></a><span data-ttu-id="8b81d-103">IWICMetadataQueryWriter \_ RemoveMetadataByName \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="8b81d-103">IWICMetadataQueryWriter\_RemoveMetadataByName\_Proxy function</span></span>

<span data-ttu-id="8b81d-104">[**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="8b81d-104">Proxy function for the [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b81d-105">語法</span><span class="sxs-lookup"><span data-stu-id="8b81d-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_RemoveMetadataByName_Proxy(
  _In_ IWICMetadataQueryWriter *THIS_PTR,
  _In_ LPCWSTR                 wzName
);
```



## <a name="parameters"></a><span data-ttu-id="8b81d-106">參數</span><span class="sxs-lookup"><span data-stu-id="8b81d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b81d-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="8b81d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b81d-108">類型： \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="8b81d-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="8b81d-109">這個 [_ *IWICMetadataQueryWriter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="8b81d-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="8b81d-110">*wzName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b81d-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b81d-111">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="8b81d-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="8b81d-112">要移除之中繼資料專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b81d-112">The name of the metadata item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b81d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b81d-113">Return value</span></span>

<span data-ttu-id="8b81d-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8b81d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8b81d-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8b81d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8b81d-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8b81d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b81d-117">備註</span><span class="sxs-lookup"><span data-stu-id="8b81d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8b81d-118">需求</span><span class="sxs-lookup"><span data-stu-id="8b81d-118">Requirements</span></span>



| <span data-ttu-id="8b81d-119">需求</span><span class="sxs-lookup"><span data-stu-id="8b81d-119">Requirement</span></span> | <span data-ttu-id="8b81d-120">值</span><span class="sxs-lookup"><span data-stu-id="8b81d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b81d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b81d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8b81d-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b81d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8b81d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b81d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8b81d-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b81d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8b81d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8b81d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b81d-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b81d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




