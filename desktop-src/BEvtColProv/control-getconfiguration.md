---
description: 讀取收集器的主動式設定。
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: Control 類別的 GetConfiguration 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5adfedb833043ffc56da09c7bdab95c1c4698587
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936068"
---
# <a name="getconfiguration-method-of-the-control-class"></a><span data-ttu-id="78c75-103">Control 類別的 GetConfiguration 方法</span><span class="sxs-lookup"><span data-stu-id="78c75-103">GetConfiguration method of the Control class</span></span>

<span data-ttu-id="78c75-104">讀取收集器的主動式設定。</span><span class="sxs-lookup"><span data-stu-id="78c75-104">Read the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c75-105">語法</span><span class="sxs-lookup"><span data-stu-id="78c75-105">Syntax</span></span>


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a><span data-ttu-id="78c75-106">參數</span><span class="sxs-lookup"><span data-stu-id="78c75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78c75-107">*TimestampLow* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="78c75-107">*TimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78c75-108">當此方法傳回時，此參數會包含時間戳記的低序位位，指出設定的設定時間。</span><span class="sxs-lookup"><span data-stu-id="78c75-108">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> <dt>

<span data-ttu-id="78c75-109">*TimestampHigh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="78c75-109">*TimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78c75-110">當此方法傳回時，此參數會包含時間戳記的高序位位，指出設定的設定時間。</span><span class="sxs-lookup"><span data-stu-id="78c75-110">When this method returns, this parameter contains the high-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78c75-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="78c75-111">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="78c75-112">0</span><span class="sxs-lookup"><span data-stu-id="78c75-112">0</span></span>

<span data-ttu-id="78c75-113">失敗</span><span class="sxs-lookup"><span data-stu-id="78c75-113">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="78c75-114">1</span><span class="sxs-lookup"><span data-stu-id="78c75-114">1</span></span>

<span data-ttu-id="78c75-115">Success</span><span class="sxs-lookup"><span data-stu-id="78c75-115">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78c75-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="78c75-116">Requirements</span></span>



| <span data-ttu-id="78c75-117">需求</span><span class="sxs-lookup"><span data-stu-id="78c75-117">Requirement</span></span> | <span data-ttu-id="78c75-118">值</span><span class="sxs-lookup"><span data-stu-id="78c75-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c75-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78c75-119">Minimum supported client</span></span><br/> | <span data-ttu-id="78c75-120">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78c75-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="78c75-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78c75-121">Minimum supported server</span></span><br/> | <span data-ttu-id="78c75-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="78c75-122">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="78c75-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="78c75-123">Namespace</span></span><br/>                | <span data-ttu-id="78c75-124">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="78c75-124">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="78c75-125">MOF</span><span class="sxs-lookup"><span data-stu-id="78c75-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78c75-126"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="78c75-126"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="78c75-127">DLL</span><span class="sxs-lookup"><span data-stu-id="78c75-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78c75-128"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78c75-128"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="78c75-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78c75-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c75-130">**控制**</span><span class="sxs-lookup"><span data-stu-id="78c75-130">**Control**</span></span>](control.md)
</dt> </dl>

 

 




