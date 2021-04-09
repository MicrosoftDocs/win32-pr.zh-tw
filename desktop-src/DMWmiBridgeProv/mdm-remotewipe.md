---
title: MDM_RemoteWipe 類別
description: MDM \_ RemoteWipe 類別允許遠端抹除裝置。
ms.assetid: 8c7c8705-8694-4ce3-ba21-ca610fe1f547
keywords:
- MDM_RemoteWipe 類別
- MDM_RemoteWipe 類別，描述
topic_type:
- apiref
api_name:
- MDM_RemoteWipe
- MDM_RemoteWipe.InstanceID
- MDM_RemoteWipe.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ece626fca573e34cf938105f5e59b61e0585fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024629"
---
# <a name="mdm_remotewipe-class"></a><span data-ttu-id="a7400-105">MDM \_ RemoteWipe 類別</span><span class="sxs-lookup"><span data-stu-id="a7400-105">MDM\_RemoteWipe class</span></span>

<span data-ttu-id="a7400-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a7400-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a7400-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a7400-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a7400-108">**MDM \_ RemoteWipe** 類別允許遠端抹除裝置。</span><span class="sxs-lookup"><span data-stu-id="a7400-108">The **MDM\_RemoteWipe** class allows a remote wipe of a device.</span></span>

<span data-ttu-id="a7400-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a7400-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7400-110">語法</span><span class="sxs-lookup"><span data-stu-id="a7400-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_RemoteWipe
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="a7400-111">成員</span><span class="sxs-lookup"><span data-stu-id="a7400-111">Members</span></span>

<span data-ttu-id="a7400-112">**MDM \_ RemoteWipe** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a7400-112">The **MDM\_RemoteWipe** class has these types of members:</span></span>

-   [<span data-ttu-id="a7400-113">方法</span><span class="sxs-lookup"><span data-stu-id="a7400-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="a7400-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a7400-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a7400-115">方法</span><span class="sxs-lookup"><span data-stu-id="a7400-115">Methods</span></span>

<span data-ttu-id="a7400-116">**MDM \_ RemoteWipe** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a7400-116">The **MDM\_RemoteWipe** class has these methods.</span></span>



| <span data-ttu-id="a7400-117">方法</span><span class="sxs-lookup"><span data-stu-id="a7400-117">Method</span></span>                                              | <span data-ttu-id="a7400-118">描述</span><span class="sxs-lookup"><span data-stu-id="a7400-118">Description</span></span>                                              |
|:----------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="a7400-119">**doWipeMethod**</span><span class="sxs-lookup"><span data-stu-id="a7400-119">**doWipeMethod**</span></span>](mdm-remotewipe-dowipemethod.md) | <span data-ttu-id="a7400-120">觸發裝置以啟動遠端清除。</span><span class="sxs-lookup"><span data-stu-id="a7400-120">Triggers the device to start the remote wipe.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a7400-121">屬性</span><span class="sxs-lookup"><span data-stu-id="a7400-121">Properties</span></span>

<span data-ttu-id="a7400-122">**MDM \_ RemoteWipe** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a7400-122">The **MDM\_RemoteWipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7400-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a7400-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7400-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7400-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7400-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7400-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7400-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a7400-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a7400-127">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7400-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="a7400-128">此類別的字串為 "RemoteWipe"。</span><span class="sxs-lookup"><span data-stu-id="a7400-128">For this class, the string is "RemoteWipe".</span></span>

</dd> <dt>

<span data-ttu-id="a7400-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a7400-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7400-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7400-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7400-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7400-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7400-132">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a7400-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a7400-133">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a7400-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="a7400-134">此類別的字串為 "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="a7400-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="a7400-135">範例</span><span class="sxs-lookup"><span data-stu-id="a7400-135">Example</span></span>

<span data-ttu-id="a7400-136">下列範例示範如何使用 RemoteWipe 並叫用 doWipeMethod。</span><span class="sxs-lookup"><span data-stu-id="a7400-136">The following example demonstrates how to use the RemoteWipe and invoke the doWipeMethod.</span></span>

> [!Note]  
> <span data-ttu-id="a7400-137">這個範例必須在本機系統使用者下執行。</span><span class="sxs-lookup"><span data-stu-id="a7400-137">This example must be executed under local system user.</span></span> <span data-ttu-id="a7400-138">若要這樣做，請從 <https://technet.microsoft.com/sysinternals/bb897553.aspx> `psexec.exe -i -s cmd.exe` 已提升許可權的系統管理命令提示字元中下載 psexec 工具，然後執行。</span><span class="sxs-lookup"><span data-stu-id="a7400-138">To do that, download the psexec tool from <https://technet.microsoft.com/sysinternals/bb897553.aspx> and run `psexec.exe -i -s cmd.exe` from an elevated admin command prompt.</span></span>

 

``` syntax
$namespaceName = "root\cimv2\mdm\dmmap"
$className = "MDM_RemoteWipe"
$methodName = "doWipeMethod"

$session = New-CimSession

$params = New-Object Microsoft.Management.Infrastructure.CimMethodParametersCollection
$param = [Microsoft.Management.Infrastructure.CimMethodParameter]::Create("param", "", "String", "In")
$params.Add($param)

try
{
    $instance = Get-CimInstance -Namespace $namespaceName -ClassName $className -Filter "ParentID='./Vendor/MSFT' and InstanceID='RemoteWipe'"
    $session.InvokeMethod($namespaceName, $instance, $methodName, $params)
}
catch [Exception]
{
    write-host $_ | out-string
}
```

## <a name="requirements"></a><span data-ttu-id="a7400-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7400-139">Requirements</span></span>



| <span data-ttu-id="a7400-140">需求</span><span class="sxs-lookup"><span data-stu-id="a7400-140">Requirement</span></span> | <span data-ttu-id="a7400-141">值</span><span class="sxs-lookup"><span data-stu-id="a7400-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7400-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7400-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a7400-143">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7400-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7400-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7400-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a7400-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="a7400-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a7400-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="a7400-146">Namespace</span></span><br/>                | <span data-ttu-id="a7400-147">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="a7400-147">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="a7400-148">MOF</span><span class="sxs-lookup"><span data-stu-id="a7400-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7400-149"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7400-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7400-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a7400-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7400-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7400-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7400-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7400-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7400-153">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="a7400-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

