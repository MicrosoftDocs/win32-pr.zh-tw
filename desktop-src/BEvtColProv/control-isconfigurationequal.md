---
description: 將引數與收集器的使用中設定進行比較。
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Control 類別的 IsConfigurationEqual 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: fb471f144a39519f1f724db458b57b624db2846d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688571"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a><span data-ttu-id="a7ccf-103">Control 類別的 IsConfigurationEqual 方法</span><span class="sxs-lookup"><span data-stu-id="a7ccf-103">IsConfigurationEqual method of the Control class</span></span>

<span data-ttu-id="a7ccf-104">將引數與收集器的使用中設定進行比較。</span><span class="sxs-lookup"><span data-stu-id="a7ccf-104">Compare the argument with the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7ccf-105">語法</span><span class="sxs-lookup"><span data-stu-id="a7ccf-105">Syntax</span></span>


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a><span data-ttu-id="a7ccf-106">參數</span><span class="sxs-lookup"><span data-stu-id="a7ccf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7ccf-107">*Config* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7ccf-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ccf-108">要與現用設定比較的設定。</span><span class="sxs-lookup"><span data-stu-id="a7ccf-108">The configuration to compare to the active configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7ccf-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7ccf-109">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="a7ccf-110">0</span><span class="sxs-lookup"><span data-stu-id="a7ccf-110">0</span></span>

<span data-ttu-id="a7ccf-111">失敗</span><span class="sxs-lookup"><span data-stu-id="a7ccf-111">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a7ccf-112">1</span><span class="sxs-lookup"><span data-stu-id="a7ccf-112">1</span></span>

<span data-ttu-id="a7ccf-113">Success</span><span class="sxs-lookup"><span data-stu-id="a7ccf-113">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7ccf-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7ccf-114">Requirements</span></span>



| <span data-ttu-id="a7ccf-115">需求</span><span class="sxs-lookup"><span data-stu-id="a7ccf-115">Requirement</span></span> | <span data-ttu-id="a7ccf-116">值</span><span class="sxs-lookup"><span data-stu-id="a7ccf-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ccf-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7ccf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a7ccf-118">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7ccf-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a7ccf-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7ccf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a7ccf-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a7ccf-120">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="a7ccf-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="a7ccf-121">Namespace</span></span><br/>                | <span data-ttu-id="a7ccf-122">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="a7ccf-122">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="a7ccf-123">MOF</span><span class="sxs-lookup"><span data-stu-id="a7ccf-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7ccf-124"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7ccf-124"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7ccf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a7ccf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7ccf-126"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a7ccf-126"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a7ccf-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7ccf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ccf-128">**控制**</span><span class="sxs-lookup"><span data-stu-id="a7ccf-128">**Control**</span></span>](control.md)
</dt> </dl>

 

 




