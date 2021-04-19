---
description: 關閉透過 StoreHandle 屬性取得的 HCERTSTORE 控制碼。
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: ICertStore：： CloseHandle 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987852"
---
# <a name="icertstoreclosehandle-method"></a><span data-ttu-id="550b1-103">ICertStore：： CloseHandle 方法</span><span class="sxs-lookup"><span data-stu-id="550b1-103">ICertStore::CloseHandle method</span></span>

<span data-ttu-id="550b1-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。\]</span><span class="sxs-lookup"><span data-stu-id="550b1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="550b1-105">**CloseHandle** 方法會關閉透過 [**StoreHandle**](icertstore-storehandle.md)屬性取得的 HCERTSTORE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="550b1-105">The **CloseHandle** method closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="550b1-106">語法</span><span class="sxs-lookup"><span data-stu-id="550b1-106">Syntax</span></span>


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a><span data-ttu-id="550b1-107">參數</span><span class="sxs-lookup"><span data-stu-id="550b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="550b1-108">*hCertStore* \[在\]</span><span class="sxs-lookup"><span data-stu-id="550b1-108">*hCertStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="550b1-109">要關閉的 HCERTSTORE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="550b1-109">The HCERTSTORE handle to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="550b1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="550b1-110">Return value</span></span>

<span data-ttu-id="550b1-111">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="550b1-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="550b1-112">S 的值 **表示 \_** 成功。</span><span class="sxs-lookup"><span data-stu-id="550b1-112">A value of **S\_OK** indicates success.</span></span> <span data-ttu-id="550b1-113">任何其他值則表示作業失敗。</span><span class="sxs-lookup"><span data-stu-id="550b1-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="550b1-114">備註</span><span class="sxs-lookup"><span data-stu-id="550b1-114">Remarks</span></span>

<span data-ttu-id="550b1-115">這個方法不會釋放 [**存放區**](store.md) 物件內所包含的 HCERTSTORE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="550b1-115">This method does not release the HCERTSTORE handle contained within a [**Store**](store.md) object.</span></span> <span data-ttu-id="550b1-116">它只能用來釋放透過 [**StoreHandle**](icertstore-storehandle.md) 屬性取得的 HCERTSTORE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="550b1-116">It should be used only to release a HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="550b1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="550b1-117">Requirements</span></span>



| <span data-ttu-id="550b1-118">需求</span><span class="sxs-lookup"><span data-stu-id="550b1-118">Requirement</span></span> | <span data-ttu-id="550b1-119">值</span><span class="sxs-lookup"><span data-stu-id="550b1-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="550b1-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="550b1-120">Redistributable</span></span><br/> | <span data-ttu-id="550b1-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="550b1-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="550b1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="550b1-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="550b1-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="550b1-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="550b1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="550b1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="550b1-125">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="550b1-125">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




