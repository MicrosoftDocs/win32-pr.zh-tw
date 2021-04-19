---
description: 啟用此隨插即用裝置。
ms.assetid: 8f2096c4-03b4-4005-9b97-0086f2b41080
ms.tgt_platform: multiple
title: Enable Win32_PnPEntity 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f64c833a29f4df3b353a7e9782ffea39396cece
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971953"
---
# <a name="enable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="8730c-103">Enable Win32 \_ PnPEntity 類別的方法</span><span class="sxs-lookup"><span data-stu-id="8730c-103">Enable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="8730c-104">啟用此隨插即用裝置。</span><span class="sxs-lookup"><span data-stu-id="8730c-104">Enables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8730c-105">語法</span><span class="sxs-lookup"><span data-stu-id="8730c-105">Syntax</span></span>


```mof
Uint32 Enable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="8730c-106">參數</span><span class="sxs-lookup"><span data-stu-id="8730c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8730c-107">*rebootNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8730c-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8730c-108">是否需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="8730c-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8730c-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="8730c-109">Requirements</span></span>



| <span data-ttu-id="8730c-110">需求</span><span class="sxs-lookup"><span data-stu-id="8730c-110">Requirement</span></span> | <span data-ttu-id="8730c-111">值</span><span class="sxs-lookup"><span data-stu-id="8730c-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8730c-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8730c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8730c-113">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8730c-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8730c-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8730c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8730c-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8730c-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="8730c-116">命名空間</span><span class="sxs-lookup"><span data-stu-id="8730c-116">Namespace</span></span><br/>                | <span data-ttu-id="8730c-117">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8730c-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8730c-118">MOF</span><span class="sxs-lookup"><span data-stu-id="8730c-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8730c-119"><dt>Cimwin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8730c-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8730c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8730c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8730c-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8730c-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8730c-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8730c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8730c-123">**Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="8730c-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




