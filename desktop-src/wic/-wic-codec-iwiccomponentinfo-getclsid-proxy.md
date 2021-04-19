---
description: GetCLSID 方法的 Proxy 函式。
ms.assetid: c6a8d752-590f-43d6-bac8-72b5bd259ad0
title: IWICComponentInfo_GetCLSID_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetCLSID_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc63d3f30605c0f5343502bcb96e989cc8496540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981886"
---
# <a name="iwiccomponentinfo_getclsid_proxy-function"></a><span data-ttu-id="589b9-103">IWICComponentInfo \_ GetCLSID \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="589b9-103">IWICComponentInfo\_GetCLSID\_Proxy function</span></span>

<span data-ttu-id="589b9-104">[**GetCLSID**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="589b9-104">Proxy function for the [**GetCLSID**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="589b9-105">語法</span><span class="sxs-lookup"><span data-stu-id="589b9-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetCLSID_Proxy(
  _In_  IWICComponentInfo *THIS_PTR,
  _Out_ CLSID             *pclsid
);
```



## <a name="parameters"></a><span data-ttu-id="589b9-106">參數</span><span class="sxs-lookup"><span data-stu-id="589b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="589b9-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="589b9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="589b9-108">類型： \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="589b9-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="589b9-109">這個 [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="589b9-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="589b9-110">*pclsid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="589b9-110">*pclsid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="589b9-111">類型： \**CLSID \** _</span><span class="sxs-lookup"><span data-stu-id="589b9-111">Type: \**CLSID\** _</span></span>

<span data-ttu-id="589b9-112">接收元件 CLSID 的指標。</span><span class="sxs-lookup"><span data-stu-id="589b9-112">A pointer that receives the component's CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="589b9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="589b9-113">Return value</span></span>

<span data-ttu-id="589b9-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="589b9-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="589b9-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="589b9-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="589b9-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="589b9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="589b9-117">備註</span><span class="sxs-lookup"><span data-stu-id="589b9-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="589b9-118">需求</span><span class="sxs-lookup"><span data-stu-id="589b9-118">Requirements</span></span>



| <span data-ttu-id="589b9-119">需求</span><span class="sxs-lookup"><span data-stu-id="589b9-119">Requirement</span></span> | <span data-ttu-id="589b9-120">值</span><span class="sxs-lookup"><span data-stu-id="589b9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="589b9-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="589b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="589b9-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="589b9-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="589b9-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="589b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="589b9-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="589b9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="589b9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="589b9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="589b9-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="589b9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




