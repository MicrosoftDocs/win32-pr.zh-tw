---
description: 建立可執行 IWICColorTransform 的色彩轉換物件。 這個 COM 物件支援無限制執行緒的物件模型。
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: WICCreateColorTransform_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995644"
---
# <a name="wiccreatecolortransform_proxy-function"></a><span data-ttu-id="c7de6-104">WICCreateColorTransform \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="c7de6-104">WICCreateColorTransform\_Proxy function</span></span>

<span data-ttu-id="c7de6-105">建立可執行 [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform)的色彩轉換物件。</span><span class="sxs-lookup"><span data-stu-id="c7de6-105">Creates an color transform object that implements [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform).</span></span> <span data-ttu-id="c7de6-106">這個 COM 物件支援無限制執行緒的物件模型。</span><span class="sxs-lookup"><span data-stu-id="c7de6-106">This COM object supports the free-threaded object model.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7de6-107">語法</span><span class="sxs-lookup"><span data-stu-id="c7de6-107">Syntax</span></span>


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a><span data-ttu-id="c7de6-108">參數</span><span class="sxs-lookup"><span data-stu-id="c7de6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7de6-109">*ppIColorTransform* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c7de6-109">*ppIColorTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7de6-110">建立的色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="c7de6-110">The color transform created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7de6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7de6-111">Return value</span></span>

<span data-ttu-id="c7de6-112">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c7de6-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c7de6-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c7de6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7de6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7de6-114">Requirements</span></span>



| <span data-ttu-id="c7de6-115">需求</span><span class="sxs-lookup"><span data-stu-id="c7de6-115">Requirement</span></span> | <span data-ttu-id="c7de6-116">值</span><span class="sxs-lookup"><span data-stu-id="c7de6-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7de6-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c7de6-117">DLL</span></span><br/> | <dl> <span data-ttu-id="c7de6-118"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7de6-118"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 
