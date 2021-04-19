---
description: 代表藉由呼叫 RoRegisterActivationFactories 函式註冊的啟用 factory。
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: 'RO_REGISTRATION_COOKIE (Roapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995820"
---
# <a name="ro_registration_cookie"></a><span data-ttu-id="6e626-103">RO \_ 註冊 \_ COOKIE</span><span class="sxs-lookup"><span data-stu-id="6e626-103">RO\_REGISTRATION\_COOKIE</span></span>

<span data-ttu-id="6e626-104">代表藉由呼叫 [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) 函式註冊的啟用 factory。</span><span class="sxs-lookup"><span data-stu-id="6e626-104">Represents activation factories that are registered by calling the [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function.</span></span>


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a><span data-ttu-id="6e626-105">備註</span><span class="sxs-lookup"><span data-stu-id="6e626-105">Remarks</span></span>

<span data-ttu-id="6e626-106">當已向 Windows 執行階段註冊可啟動的類別 factory 時， [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) 函數會傳回 **RO \_ 註冊 \_ COOKIE** 。</span><span class="sxs-lookup"><span data-stu-id="6e626-106">The [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function returns a **RO\_REGISTRATION\_COOKIE** when a activatable class factories are registered with the Windows Runtime.</span></span> <span data-ttu-id="6e626-107">[**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)函式會使用 cookie 來移除 class factory。</span><span class="sxs-lookup"><span data-stu-id="6e626-107">The [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) function uses the cookie to remove the class factories.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e626-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e626-108">Requirements</span></span>



| <span data-ttu-id="6e626-109">需求</span><span class="sxs-lookup"><span data-stu-id="6e626-109">Requirement</span></span> | <span data-ttu-id="6e626-110">值</span><span class="sxs-lookup"><span data-stu-id="6e626-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e626-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e626-111">Minimum supported client</span></span><br/> | <span data-ttu-id="6e626-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e626-112">Windows 8</span></span><br/>                                                               |
| <span data-ttu-id="6e626-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e626-113">Minimum supported server</span></span><br/> | <span data-ttu-id="6e626-114">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e626-114">Windows Server 2012</span></span><br/>                                                     |
| <span data-ttu-id="6e626-115">標頭</span><span class="sxs-lookup"><span data-stu-id="6e626-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e626-116"><dt>Roapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e626-116"><dt>Roapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e626-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e626-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e626-118">**RoRegisterActivationFactories**</span><span class="sxs-lookup"><span data-stu-id="6e626-118">**RoRegisterActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[<span data-ttu-id="6e626-119">**RoRevokeActivationFactories**</span><span class="sxs-lookup"><span data-stu-id="6e626-119">**RoRevokeActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
