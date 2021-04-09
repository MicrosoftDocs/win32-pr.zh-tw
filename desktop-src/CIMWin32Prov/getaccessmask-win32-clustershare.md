---
description: 傳回具有使用者或群組所持有之共用的存取權限的 uint32 點陣圖，而該共用會傳回該實例。
ms.assetid: 1f656c63-f5ee-4b14-845a-0eb34a0e7a64
ms.tgt_platform: multiple
title: Win32_ClusterShare 類別的 GetAccessMask 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: db27998c362e3df350dd12b6b91f3966cfc152ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110509"
---
# <a name="getaccessmask-method-of-the-win32_clustershare-class"></a><span data-ttu-id="10bac-103">Win32 ClusterShare 類別的 GetAccessMask 方法 \_</span><span class="sxs-lookup"><span data-stu-id="10bac-103">GetAccessMask method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="10bac-104">傳回具有使用者或群組所持有之共用的存取權限的 **uint32** 點陣圖，而該共用會傳回該實例。</span><span class="sxs-lookup"><span data-stu-id="10bac-104">Returns a **uint32** bitmap with the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="10bac-105">語法</span><span class="sxs-lookup"><span data-stu-id="10bac-105">Syntax</span></span>


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a><span data-ttu-id="10bac-106">參數</span><span class="sxs-lookup"><span data-stu-id="10bac-106">Parameters</span></span>

<span data-ttu-id="10bac-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="10bac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10bac-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="10bac-108">Return value</span></span>

<span data-ttu-id="10bac-109">使用者或群組所持有之共用的存取權限。</span><span class="sxs-lookup"><span data-stu-id="10bac-109">Access rights to the share held by the user or group.</span></span>

## <a name="requirements"></a><span data-ttu-id="10bac-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="10bac-110">Requirements</span></span>



| <span data-ttu-id="10bac-111">需求</span><span class="sxs-lookup"><span data-stu-id="10bac-111">Requirement</span></span> | <span data-ttu-id="10bac-112">值</span><span class="sxs-lookup"><span data-stu-id="10bac-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10bac-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10bac-113">Minimum supported client</span></span><br/> | <span data-ttu-id="10bac-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="10bac-114">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="10bac-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10bac-115">Minimum supported server</span></span><br/> | <span data-ttu-id="10bac-116">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10bac-116">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="10bac-117">命名空間</span><span class="sxs-lookup"><span data-stu-id="10bac-117">Namespace</span></span><br/>                | <span data-ttu-id="10bac-118">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="10bac-118">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10bac-119">MOF</span><span class="sxs-lookup"><span data-stu-id="10bac-119">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10bac-120"><dt>Cimwin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="10bac-120"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10bac-121">DLL</span><span class="sxs-lookup"><span data-stu-id="10bac-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10bac-122"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10bac-122"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10bac-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10bac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10bac-124">**Win32 \_ ClusterShare**</span><span class="sxs-lookup"><span data-stu-id="10bac-124">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

 




