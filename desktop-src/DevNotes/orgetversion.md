---
description: 此函式會捕獲離線登錄庫的版本。
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: 'ORGetVersion 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978719"
---
# <a name="orgetversion-function"></a><span data-ttu-id="aa6bb-103">ORGetVersion 函式</span><span class="sxs-lookup"><span data-stu-id="aa6bb-103">ORGetVersion function</span></span>

<span data-ttu-id="aa6bb-104">此函式會捕獲離線登錄庫的版本。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-104">This function retrieves the version of the offline registry library.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa6bb-105">語法</span><span class="sxs-lookup"><span data-stu-id="aa6bb-105">Syntax</span></span>


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="aa6bb-106">參數</span><span class="sxs-lookup"><span data-stu-id="aa6bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa6bb-107">*pdwMajorVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="aa6bb-107">*pdwMajorVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6bb-108">變數的指標，用來接收離線登錄庫的主要版本。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-108">A pointer to a variable to receive the major version of the offline registry library.</span></span> <span data-ttu-id="aa6bb-109">針對程式庫的初始版本，值為1。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-109">For the initial release of the library, the value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="aa6bb-110">*pdwMinorVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="aa6bb-110">*pdwMinorVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6bb-111">變數的指標，用來接收離線登錄庫的次要版本。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-111">A pointer to a variable to receive the minor version of the offline registry library.</span></span> <span data-ttu-id="aa6bb-112">若為程式庫的初始版本，此值為0。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-112">For the initial release of the library, the value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa6bb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa6bb-113">Return value</span></span>

<span data-ttu-id="aa6bb-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa6bb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa6bb-115">Requirements</span></span>



| <span data-ttu-id="aa6bb-116">需求</span><span class="sxs-lookup"><span data-stu-id="aa6bb-116">Requirement</span></span> | <span data-ttu-id="aa6bb-117">值</span><span class="sxs-lookup"><span data-stu-id="aa6bb-117">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa6bb-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="aa6bb-118">Redistributable</span></span><br/> | <span data-ttu-id="aa6bb-119">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="aa6bb-119">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="aa6bb-120">標頭</span><span class="sxs-lookup"><span data-stu-id="aa6bb-120">Header</span></span><br/>          | <dl> <span data-ttu-id="aa6bb-121"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa6bb-121"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa6bb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="aa6bb-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="aa6bb-123"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa6bb-123"><dt>Offreg.dll</dt></span></span> </dl> |



 

 




