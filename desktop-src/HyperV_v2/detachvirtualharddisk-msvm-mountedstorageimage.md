---
description: 卸離與這個類別相關聯的已掛接儲存映射。
ms.assetid: C3AB0EEE-71FE-4049-90AB-01F5D77E3B97
title: Msvm_MountedStorageImage 類別的 DetachVirtualHardDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage.DetachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0d411134d85fe70163b2e08eebed0ff0d4b88e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985263"
---
# <a name="detachvirtualharddisk-method-of-the-msvm_mountedstorageimage-class"></a><span data-ttu-id="26530-103">Msvm MountedStorageImage 類別的 DetachVirtualHardDisk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="26530-103">DetachVirtualHardDisk method of the Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="26530-104">卸離與這個類別相關聯的已掛接儲存映射。</span><span class="sxs-lookup"><span data-stu-id="26530-104">Detaches the mounted storage image that is associated with this class.</span></span>

## <a name="syntax"></a><span data-ttu-id="26530-105">語法</span><span class="sxs-lookup"><span data-stu-id="26530-105">Syntax</span></span>


```mof
uint32 DetachVirtualHardDisk();
```



## <a name="parameters"></a><span data-ttu-id="26530-106">參數</span><span class="sxs-lookup"><span data-stu-id="26530-106">Parameters</span></span>

<span data-ttu-id="26530-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="26530-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26530-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="26530-108">Return value</span></span>

<span data-ttu-id="26530-109">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="26530-109">Type: **uint32**</span></span>

<span data-ttu-id="26530-110">這個方法可能會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="26530-110">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="26530-111">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="26530-111">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="26530-112">**失敗** (1) </span><span class="sxs-lookup"><span data-stu-id="26530-112">**Failed** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="26530-113">備註</span><span class="sxs-lookup"><span data-stu-id="26530-113">Remarks</span></span>

<span data-ttu-id="26530-114">存取 [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="26530-114">Access to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="26530-115">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="26530-115">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="26530-116">範例</span><span class="sxs-lookup"><span data-stu-id="26530-116">Examples</span></span>

<span data-ttu-id="26530-117">下列 c # 範例顯示如何卸離虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="26530-117">The following C# example shows how to detach a virtual hard disk file.</span></span> <span data-ttu-id="26530-118">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="26530-118">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void DetachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);

    ManagementClass mountedStorageImageServiceClass = new ManagementClass("Msvm_MountedStorageImage");

    mountedStorageImageServiceClass.Scope = scope;

    using (ManagementObjectCollection collection = mountedStorageImageServiceClass.GetInstances())
    {
        foreach (ManagementObject image in collection)
        {
            using (image)
            {
                string name = image.GetPropertyValue("Name").ToString();
                if (string.Equals(name, path, StringComparison.OrdinalIgnoreCase))
                {
                    ManagementBaseObject outParams = image.InvokeMethod("DetachVirtualHardDisk", null, null);

                    if ((UInt32)outParams["ReturnValue"] == 0)
                    {
                        Console.WriteLine("{0} was detached successfully.", path);
                    }
                    else
                    {
                        Console.WriteLine("Unable to dettach {0}", path);
                    }

                    outParams.Dispose();

                    break;
                }

                image.Dispose();
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="26530-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="26530-119">Requirements</span></span>



| <span data-ttu-id="26530-120">需求</span><span class="sxs-lookup"><span data-stu-id="26530-120">Requirement</span></span> | <span data-ttu-id="26530-121">值</span><span class="sxs-lookup"><span data-stu-id="26530-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26530-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26530-122">Minimum supported client</span></span><br/> | <span data-ttu-id="26530-123">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26530-123">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="26530-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26530-124">Minimum supported server</span></span><br/> | <span data-ttu-id="26530-125">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26530-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26530-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="26530-126">Namespace</span></span><br/>                | <span data-ttu-id="26530-127">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="26530-127">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="26530-128">MOF</span><span class="sxs-lookup"><span data-stu-id="26530-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26530-129"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="26530-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="26530-130">DLL</span><span class="sxs-lookup"><span data-stu-id="26530-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26530-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="26530-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="26530-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26530-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26530-133">**Msvm \_ MountedStorageImage**</span><span class="sxs-lookup"><span data-stu-id="26530-133">**Msvm\_MountedStorageImage**</span></span>](msvm-mountedstorageimage.md)
</dt> </dl>

 

