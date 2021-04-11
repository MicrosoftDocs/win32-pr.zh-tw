---
description: 取得此隨插即用裝置的指定屬性。
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: Win32_PnPEntity 類別的 GetDeviceProperties 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.GetDeviceProperties
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6aa9f6cad17fe48617b5bf7d28ba19d6f5370834
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025885"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="5ed7a-103">Win32 PnPEntity 類別的 GetDeviceProperties 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5ed7a-103">GetDeviceProperties method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="5ed7a-104">取得此隨插即用裝置的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="5ed7a-104">Gets the specified properties of this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed7a-105">語法</span><span class="sxs-lookup"><span data-stu-id="5ed7a-105">Syntax</span></span>


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a><span data-ttu-id="5ed7a-106">參數</span><span class="sxs-lookup"><span data-stu-id="5ed7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed7a-107">*devicePropertyKeys* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="5ed7a-107">*devicePropertyKeys* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed7a-108">要傳回的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ed7a-108">The properties to return.</span></span>

</dd> <dt>

<span data-ttu-id="5ed7a-109">*deviceProperties* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5ed7a-109">*deviceProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed7a-110">[**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md)抽象類別的適當子類型中要求的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ed7a-110">The requested properties in appropriate subtypes of the [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md) abstract class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ed7a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ed7a-111">Requirements</span></span>



| <span data-ttu-id="5ed7a-112">需求</span><span class="sxs-lookup"><span data-stu-id="5ed7a-112">Requirement</span></span> | <span data-ttu-id="5ed7a-113">值</span><span class="sxs-lookup"><span data-stu-id="5ed7a-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed7a-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ed7a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed7a-115">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ed7a-115">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5ed7a-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ed7a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed7a-117">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5ed7a-117">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="5ed7a-118">命名空間</span><span class="sxs-lookup"><span data-stu-id="5ed7a-118">Namespace</span></span><br/>                | <span data-ttu-id="5ed7a-119">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5ed7a-119">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ed7a-120">MOF</span><span class="sxs-lookup"><span data-stu-id="5ed7a-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ed7a-121"><dt>Cimwin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ed7a-121"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ed7a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5ed7a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ed7a-123"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ed7a-123"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ed7a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ed7a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed7a-125">**Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="5ed7a-125">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




