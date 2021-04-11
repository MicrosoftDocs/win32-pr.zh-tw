---
description: CreateQueryWriterFromBlockWriter 方法的 Proxy 函式。
ms.assetid: f941e3b1-1645-4ed6-b2c5-180cb4c43fca
title: IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c8c94b351e72fd7de367e5dd74a0c7ed62ce84f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194131"
---
# <a name="iwiccomponentfactory_createquerywriterfromblockwriter_proxy-function"></a><span data-ttu-id="c29b6-103">IWICComponentFactory \_ CreateQueryWriterFromBlockWriter \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="c29b6-103">IWICComponentFactory\_CreateQueryWriterFromBlockWriter\_Proxy function</span></span>

<span data-ttu-id="c29b6-104">[**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="c29b6-104">Proxy function for the [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c29b6-105">語法</span><span class="sxs-lookup"><span data-stu-id="c29b6-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy(
  _In_  IWICComponentFactory    *THIS_PTR,
  _In_  IWICMetadataBlockWriter *pIBlockWriter,
  _Out_ IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="c29b6-106">參數</span><span class="sxs-lookup"><span data-stu-id="c29b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c29b6-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="c29b6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c29b6-108">類型： \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="c29b6-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="c29b6-109">這個 [_ *IWICComponentFactory* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="c29b6-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="c29b6-110">*pIBlockWriter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c29b6-110">*pIBlockWriter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c29b6-111">類型： \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) \** _</span><span class="sxs-lookup"><span data-stu-id="c29b6-111">Type: \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)\** _</span></span>

</dd> <dt>

<span data-ttu-id="c29b6-112">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c29b6-112">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c29b6-113">類型： **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="c29b6-113">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c29b6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c29b6-114">Return value</span></span>

<span data-ttu-id="c29b6-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c29b6-115">Type: **HRESULT**</span></span>

<span data-ttu-id="c29b6-116">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c29b6-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c29b6-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c29b6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c29b6-118">備註</span><span class="sxs-lookup"><span data-stu-id="c29b6-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c29b6-119">需求</span><span class="sxs-lookup"><span data-stu-id="c29b6-119">Requirements</span></span>



| <span data-ttu-id="c29b6-120">需求</span><span class="sxs-lookup"><span data-stu-id="c29b6-120">Requirement</span></span> | <span data-ttu-id="c29b6-121">值</span><span class="sxs-lookup"><span data-stu-id="c29b6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c29b6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c29b6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c29b6-123">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c29b6-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c29b6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c29b6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c29b6-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c29b6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c29b6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c29b6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c29b6-127"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c29b6-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




