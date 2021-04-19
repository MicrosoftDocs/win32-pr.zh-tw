---
title: ROTFlags
description: 控制在執行中的物件資料表中，COM 伺服器的註冊 (ROT) 。
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- ROTFlags 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967817"
---
# <a name="rotflags"></a><span data-ttu-id="caf28-104">ROTFlags</span><span class="sxs-lookup"><span data-stu-id="caf28-104">ROTFlags</span></span>

<span data-ttu-id="caf28-105">控制在執行中的物件資料表中，COM 伺服器的註冊 (ROT) 。</span><span class="sxs-lookup"><span data-stu-id="caf28-105">Controls the registration of a COM server in the running object table (ROT).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="caf28-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="caf28-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a><span data-ttu-id="caf28-107">備註</span><span class="sxs-lookup"><span data-stu-id="caf28-107">Remarks</span></span>

<span data-ttu-id="caf28-108">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="caf28-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="caf28-109">旗標值</span><span class="sxs-lookup"><span data-stu-id="caf28-109">Flag Value</span></span> | <span data-ttu-id="caf28-110">常數</span><span class="sxs-lookup"><span data-stu-id="caf28-110">Constant</span></span>                        |
|------------|---------------------------------|
| <span data-ttu-id="caf28-111">0x1</span><span class="sxs-lookup"><span data-stu-id="caf28-111">0x1</span></span>        | <span data-ttu-id="caf28-112">**ROTREGFLAGS \_ ALLOWANYCLIENT**</span><span class="sxs-lookup"><span data-stu-id="caf28-112">**ROTREGFLAGS\_ALLOWANYCLIENT**</span></span> |



 

### <a name="rotregflags_allowanyclient-description"></a><span data-ttu-id="caf28-113">ROTREGFLAGS \_ ALLOWANYCLIENT 描述</span><span class="sxs-lookup"><span data-stu-id="caf28-113">ROTREGFLAGS\_ALLOWANYCLIENT Description</span></span>

<span data-ttu-id="caf28-114">如果 COM 伺服器想要在 ROT 中註冊，並允許任何用戶端存取註冊，則必須使用 **ROTFLAGS \_ ALLOWANYCLIENT** 旗標。</span><span class="sxs-lookup"><span data-stu-id="caf28-114">If a COM server wants to register in the ROT and allow any client to access the registration, it must use the **ROTFLAGS\_ALLOWANYCLIENT** flag.</span></span> <span data-ttu-id="caf28-115">"Activate As Activator" COM 伺服器無法指定 **ROTFLAGS \_ ALLOWANYCLIENT** ，因為 DCOM 服務控制管理員 (DCOMSCM) 強制對此旗標進行詐騙檢查。</span><span class="sxs-lookup"><span data-stu-id="caf28-115">An "Activate As Activator" COM server cannot specify **ROTFLAGS\_ALLOWANYCLIENT** because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="caf28-116">因此，在 Windows Vista 和更新版本中，COM 新增了 **ROTFlags** 登錄專案的支援，可讓伺服器規定其衰減註冊可供任何用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="caf28-116">Therefore, in Windows Vista and later, COM adds support for the **ROTFlags** registry entry that allows the server to stipulate that its ROT registrations be made available to any client.</span></span>

<span data-ttu-id="caf28-117">專案必須存在於 **HKEY \_ 本機 \_ 電腦** hive 中。</span><span class="sxs-lookup"><span data-stu-id="caf28-117">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span> <span data-ttu-id="caf28-118">此專案提供「啟用為啟動程式」伺服器，其功能與 **ROTFLAGS \_ ALLOWANYCLIENT** 為 RunAs 伺服器提供的功能相同。</span><span class="sxs-lookup"><span data-stu-id="caf28-118">This entry provides an "Activate As Activator" server with the same functionality that **ROTFLAGS\_ALLOWANYCLIENT** provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="caf28-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="caf28-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caf28-120">AppID 金鑰</span><span class="sxs-lookup"><span data-stu-id="caf28-120">AppID Key</span></span>](appid-key.md)
</dt> <dt>

[<span data-ttu-id="caf28-121">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="caf28-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="caf28-122">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="caf28-122">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




