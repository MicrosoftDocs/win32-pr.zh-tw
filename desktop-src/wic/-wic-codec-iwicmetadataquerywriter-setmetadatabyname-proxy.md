---
description: SetMetadataByName 方法的 Proxy 函式。
ms.assetid: 467d7735-152a-4e7c-93b1-fd031cc57c19
title: IWICMetadataQueryWriter_SetMetadataByName_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_SetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e27ea57ec5b26fd2bed04ea99f6c6cbfb11c8874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001414"
---
# <a name="iwicmetadataquerywriter_setmetadatabyname_proxy-function"></a><span data-ttu-id="1e5c9-103">IWICMetadataQueryWriter \_ SetMetadataByName \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="1e5c9-103">IWICMetadataQueryWriter\_SetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="1e5c9-104">[**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="1e5c9-104">Proxy function for the [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e5c9-105">語法</span><span class="sxs-lookup"><span data-stu-id="1e5c9-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_SetMetadataByName_Proxy(
  _In_       IWICMetadataQueryWriter *THIS_PTR,
  _In_       LPCWSTR                 wzName,
  _In_ const PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="1e5c9-106">參數</span><span class="sxs-lookup"><span data-stu-id="1e5c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e5c9-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="1e5c9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e5c9-108">類型： \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="1e5c9-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="1e5c9-109">這個 [_ *IWICMetadataQueryWriter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="1e5c9-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="1e5c9-110">*wzName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e5c9-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e5c9-111">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="1e5c9-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="1e5c9-112">中繼資料專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e5c9-112">The name of the metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="1e5c9-113">*pvarValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e5c9-113">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e5c9-114">類型： \**Const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="1e5c9-114">Type: \**const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="1e5c9-115">要設定的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1e5c9-115">The metadata to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e5c9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e5c9-116">Return value</span></span>

<span data-ttu-id="1e5c9-117">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1e5c9-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1e5c9-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1e5c9-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1e5c9-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1e5c9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e5c9-120">備註</span><span class="sxs-lookup"><span data-stu-id="1e5c9-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1e5c9-121">需求</span><span class="sxs-lookup"><span data-stu-id="1e5c9-121">Requirements</span></span>



| <span data-ttu-id="1e5c9-122">需求</span><span class="sxs-lookup"><span data-stu-id="1e5c9-122">Requirement</span></span> | <span data-ttu-id="1e5c9-123">值</span><span class="sxs-lookup"><span data-stu-id="1e5c9-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e5c9-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e5c9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1e5c9-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e5c9-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1e5c9-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e5c9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1e5c9-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e5c9-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1e5c9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1e5c9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e5c9-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e5c9-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

