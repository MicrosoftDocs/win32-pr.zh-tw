---
title: sessionStateChangeType 簡單類型
description: 定義終端機伺服器會話狀態變更的值，您可以用來觸發工作開始。
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- sessionStateChangeType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a77fb563b59ccd8d63d38c6c85f16ff74ac404b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466416"
---
# <a name="sessionstatechangetype-simple-type"></a><span data-ttu-id="aad23-104">sessionStateChangeType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="aad23-104">sessionStateChangeType Simple Type</span></span>

<span data-ttu-id="aad23-105">定義終端機伺服器會話狀態變更的值，您可以用來觸發工作開始。</span><span class="sxs-lookup"><span data-stu-id="aad23-105">Defines values for the kind of Terminal Server session state change you can use to trigger a task to start.</span></span>

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="aad23-106">列舉值</span><span class="sxs-lookup"><span data-stu-id="aad23-106">Enumeration values</span></span>

<span data-ttu-id="aad23-107">**SessionStateChangeType** 簡單類型會定義下列值。</span><span class="sxs-lookup"><span data-stu-id="aad23-107">The **sessionStateChangeType** simple type defines the following values.</span></span>



| <span data-ttu-id="aad23-108">值</span><span class="sxs-lookup"><span data-stu-id="aad23-108">Value</span></span>             | <span data-ttu-id="aad23-109">描述</span><span class="sxs-lookup"><span data-stu-id="aad23-109">Description</span></span>                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aad23-110">ConsoleConnect</span><span class="sxs-lookup"><span data-stu-id="aad23-110">ConsoleConnect</span></span>    | <span data-ttu-id="aad23-111">終端機伺服器主控台連接狀態變更。</span><span class="sxs-lookup"><span data-stu-id="aad23-111">Terminal Server console connection state change.</span></span> <span data-ttu-id="aad23-112">例如，當您藉由切換電腦上的使用者，連接到本機電腦上的使用者會話時。</span><span class="sxs-lookup"><span data-stu-id="aad23-112">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                            |
| <span data-ttu-id="aad23-113">ConsoleDisconnect</span><span class="sxs-lookup"><span data-stu-id="aad23-113">ConsoleDisconnect</span></span> | <span data-ttu-id="aad23-114">終端機伺服器主控台中斷連接狀態變更。</span><span class="sxs-lookup"><span data-stu-id="aad23-114">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="aad23-115">例如，當您藉由切換電腦上的使用者，在本機電腦上中斷使用者會話的連線時。</span><span class="sxs-lookup"><span data-stu-id="aad23-115">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span> <br/>                      |
| <span data-ttu-id="aad23-116">RemoteConnect</span><span class="sxs-lookup"><span data-stu-id="aad23-116">RemoteConnect</span></span>     | <span data-ttu-id="aad23-117">終端機伺服器遠端線上狀態變更。</span><span class="sxs-lookup"><span data-stu-id="aad23-117">Terminal Server remote connection state change.</span></span> <span data-ttu-id="aad23-118">例如，當使用者從遠端電腦使用遠端桌面連線程式連接到使用者會話時。</span><span class="sxs-lookup"><span data-stu-id="aad23-118">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span> <br/>            |
| <span data-ttu-id="aad23-119">RemoteDisconnect</span><span class="sxs-lookup"><span data-stu-id="aad23-119">RemoteDisconnect</span></span>  | <span data-ttu-id="aad23-120">終端機伺服器遠端中斷連接狀態變更。</span><span class="sxs-lookup"><span data-stu-id="aad23-120">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="aad23-121">例如，當使用者從遠端電腦使用遠端桌面連線程式時，從使用者會話中斷連線。</span><span class="sxs-lookup"><span data-stu-id="aad23-121">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span> <br/> |
| <span data-ttu-id="aad23-122">SessionLock</span><span class="sxs-lookup"><span data-stu-id="aad23-122">SessionLock</span></span>       | <span data-ttu-id="aad23-123">終端機伺服器會話鎖定狀態變更。</span><span class="sxs-lookup"><span data-stu-id="aad23-123">Terminal Server session locked state change.</span></span> <span data-ttu-id="aad23-124">例如，此狀態變更會在電腦鎖定時執行工作。</span><span class="sxs-lookup"><span data-stu-id="aad23-124">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                       |
| <span data-ttu-id="aad23-125">SessionUnlock</span><span class="sxs-lookup"><span data-stu-id="aad23-125">SessionUnlock</span></span>     | <span data-ttu-id="aad23-126">終端機伺服器會話已解除鎖定狀態變更。</span><span class="sxs-lookup"><span data-stu-id="aad23-126">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="aad23-127">例如，此狀態變更會在電腦解除鎖定時，讓工作執行。</span><span class="sxs-lookup"><span data-stu-id="aad23-127">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                    |



## <a name="requirements"></a><span data-ttu-id="aad23-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="aad23-128">Requirements</span></span>



| <span data-ttu-id="aad23-129">需求</span><span class="sxs-lookup"><span data-stu-id="aad23-129">Requirement</span></span> | <span data-ttu-id="aad23-130">值</span><span class="sxs-lookup"><span data-stu-id="aad23-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aad23-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aad23-131">Minimum supported client</span></span><br/> | <span data-ttu-id="aad23-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aad23-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aad23-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aad23-133">Minimum supported server</span></span><br/> | <span data-ttu-id="aad23-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aad23-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





