---
description: Commit 方法的 Proxy 函數。
ms.assetid: f7f1be43-fe44-47eb-a5ba-3446c0db22a6
title: IWICBitmapEncoder_Commit_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0cd3cfbe5e1c80d82cd90303d26f2da33cf467d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026187"
---
# <a name="iwicbitmapencoder_commit_proxy-function"></a><span data-ttu-id="92d0f-103">IWICBitmapEncoder \_ Commit \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="92d0f-103">IWICBitmapEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="92d0f-104">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)方法的 Proxy 函數。</span><span class="sxs-lookup"><span data-stu-id="92d0f-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="92d0f-105">語法</span><span class="sxs-lookup"><span data-stu-id="92d0f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Commit_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="92d0f-106">參數</span><span class="sxs-lookup"><span data-stu-id="92d0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92d0f-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="92d0f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92d0f-108">類型： \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="92d0f-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="92d0f-109">這個 [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="92d0f-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92d0f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="92d0f-110">Return value</span></span>

<span data-ttu-id="92d0f-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="92d0f-111">Type: **HRESULT**</span></span>

<span data-ttu-id="92d0f-112">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="92d0f-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="92d0f-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="92d0f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="92d0f-114">備註</span><span class="sxs-lookup"><span data-stu-id="92d0f-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="92d0f-115">需求</span><span class="sxs-lookup"><span data-stu-id="92d0f-115">Requirements</span></span>



| <span data-ttu-id="92d0f-116">需求</span><span class="sxs-lookup"><span data-stu-id="92d0f-116">Requirement</span></span> | <span data-ttu-id="92d0f-117">值</span><span class="sxs-lookup"><span data-stu-id="92d0f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d0f-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92d0f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="92d0f-119">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92d0f-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="92d0f-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92d0f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="92d0f-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92d0f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="92d0f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="92d0f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92d0f-123"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="92d0f-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




