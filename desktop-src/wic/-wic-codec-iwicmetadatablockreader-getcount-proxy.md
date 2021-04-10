---
description: GetCount 方法的 Proxy 函式。
ms.assetid: 441bbbaf-5a6a-4d1e-bb8d-f79af6aa2708
title: IWICMetadataBlockReader_GetCount_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 09c3c33185791c2c2eefd3963a3d39977c706963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194263"
---
# <a name="iwicmetadatablockreader_getcount_proxy-function"></a><span data-ttu-id="ab18d-103">IWICMetadataBlockReader \_ GetCount \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="ab18d-103">IWICMetadataBlockReader\_GetCount\_Proxy function</span></span>

<span data-ttu-id="ab18d-104">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="ab18d-104">Proxy function for the [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab18d-105">語法</span><span class="sxs-lookup"><span data-stu-id="ab18d-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetCount_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _Out_ UINT                    *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="ab18d-106">參數</span><span class="sxs-lookup"><span data-stu-id="ab18d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab18d-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="ab18d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18d-108">類型： \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="ab18d-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="ab18d-109">這個 [_ *IWICMetadataBlockReader* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="ab18d-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="ab18d-110">*pcCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ab18d-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18d-111">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="ab18d-111">Type: \**UINT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab18d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab18d-112">Return value</span></span>

<span data-ttu-id="ab18d-113">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ab18d-113">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ab18d-114">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ab18d-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab18d-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ab18d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab18d-116">備註</span><span class="sxs-lookup"><span data-stu-id="ab18d-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ab18d-117">需求</span><span class="sxs-lookup"><span data-stu-id="ab18d-117">Requirements</span></span>



| <span data-ttu-id="ab18d-118">需求</span><span class="sxs-lookup"><span data-stu-id="ab18d-118">Requirement</span></span> | <span data-ttu-id="ab18d-119">值</span><span class="sxs-lookup"><span data-stu-id="ab18d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab18d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab18d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab18d-121">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab18d-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ab18d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab18d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab18d-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab18d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ab18d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ab18d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab18d-125"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab18d-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




