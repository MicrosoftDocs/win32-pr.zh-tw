---
description: 代表提供運算功能的集合，其中包含 CIM \_ ManagedSystemElement 物件。
ms.assetid: 410be43f-3368-4109-8b29-7b7cc2a3ec1b
title: 'CIM_ComputerSystem 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.NameFormat
- CIM_ComputerSystem.Dedicated
- CIM_ComputerSystem.OtherDedicatedDescriptions
- CIM_ComputerSystem.ResetCapability
- CIM_ComputerSystem.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00a53d0c514113175c3c6ffb7ea40f8ef4e730d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976569"
---
# <a name="cim_computersystem-class-hyper-v-management"></a><span data-ttu-id="ad6fc-103">CIM_ComputerSystem 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-103">CIM_ComputerSystem class (Hyper-V management)</span></span>

<span data-ttu-id="ad6fc-104">代表提供運算功能的集合，其中包含 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-104">Represents a collection that provides computing capabilities and consists of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad6fc-105">語法</span><span class="sxs-lookup"><span data-stu-id="ad6fc-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string NameFormat;
  uint16 Dedicated[];
  string OtherDedicatedDescriptions[];
  uint16 ResetCapability;
  uint16 PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="ad6fc-106">成員</span><span class="sxs-lookup"><span data-stu-id="ad6fc-106">Members</span></span>

<span data-ttu-id="ad6fc-107">**CIM 同 \_** 型類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ad6fc-107">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="ad6fc-108">方法</span><span class="sxs-lookup"><span data-stu-id="ad6fc-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="ad6fc-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ad6fc-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ad6fc-110">方法</span><span class="sxs-lookup"><span data-stu-id="ad6fc-110">Methods</span></span>

<span data-ttu-id="ad6fc-111">**CIM 的 \_** 程式類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-111">The **CIM\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="ad6fc-112">方法</span><span class="sxs-lookup"><span data-stu-id="ad6fc-112">Method</span></span>                                                    | <span data-ttu-id="ad6fc-113">描述</span><span class="sxs-lookup"><span data-stu-id="ad6fc-113">Description</span></span>                                                                                                                                                                                                          |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad6fc-114">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ad6fc-114">**SetPowerState**</span></span>](cim-computersystem-setpowerstate.md) | <span data-ttu-id="ad6fc-115">此方法已被取代。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-115">This method is deprecated.</span></span> <span data-ttu-id="ad6fc-116">請改為使用 **CIM \_ PowerManagementService** 類別中的 **RequestPowerStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-116">Instead, use the **RequestPowerStateChange** method in the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="ad6fc-117">已 **淘汰的描述：** 設定電腦的電源狀態。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-117">**Deprecated description:** Sets the power state of the computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ad6fc-118">屬性</span><span class="sxs-lookup"><span data-stu-id="ad6fc-118">Properties</span></span>

<span data-ttu-id="ad6fc-119">**CIM 無 \_** 類別類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-119">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad6fc-120">**專用**</span><span class="sxs-lookup"><span data-stu-id="ad6fc-120">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6fc-121">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ad6fc-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ad6fc-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad6fc-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6fc-123">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \|MIB-II.sysServices」、「FC-GS」。INCITS-T11 \| Platform \| PlatformType ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_** 宏。**OtherDedicatedDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="ad6fc-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.sysServices", "FC-GS.INCITS-T11 \| Platform \| PlatformType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**OtherDedicatedDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="ad6fc-124">電腦系統的用途和功能。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-124">The purpose and features of the computer system.</span></span> <span data-ttu-id="ad6fc-125">例如，專用於列印的系統可以指定 "11" (列印) 。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-125">For example, a system dedicated to printing could specify "11" (Print).</span></span> <span data-ttu-id="ad6fc-126">具有列印功能的一般目的系統可以設定為「0」 (非專用) 和「11」 (列印) 。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-126">A general purpose system with printing capabilities can be set to "0" (Not Dedicated) and "11" (Print).</span></span>

<dt>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>

<span data-ttu-id="ad6fc-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**非專用** (0) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Not Dedicated** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ad6fc-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ad6fc-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (2) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="ad6fc-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**儲存體** (3) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>

<span data-ttu-id="ad6fc-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**路由器** (4) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Router** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="ad6fc-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**切換** (5) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>

<span data-ttu-id="ad6fc-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>第 **3 層交換器** (6) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Layer 3 Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>

<span data-ttu-id="ad6fc-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**中央辦公室交換器** (7) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Central Office Switch** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>

<span data-ttu-id="ad6fc-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**中樞** (8) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>

<span data-ttu-id="ad6fc-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**存取伺服器** (9) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Access Server** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>

<span data-ttu-id="ad6fc-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**防火牆** (10) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="ad6fc-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**列印** (11) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Print** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O"></span><span id="i_o"></span>

<span data-ttu-id="ad6fc-139"><span id="I_O"></span><span id="i_o"></span>**I/o** (12) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-139"><span id="I_O"></span><span id="i_o"></span>**I/O** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>

<span data-ttu-id="ad6fc-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Web Caching** (13) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Web Caching** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>

<span data-ttu-id="ad6fc-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**管理** (14) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Management** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ad6fc-142">此實例專門用來裝載系統管理軟體</span><span class="sxs-lookup"><span data-stu-id="ad6fc-142">This instance is dedicated to hosting system management software</span></span>

</dd> <dt>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>

<span data-ttu-id="ad6fc-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**封鎖伺服器** (15) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Block Server** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>

<span data-ttu-id="ad6fc-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**檔案伺服器** (16) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**File Server** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>

<span data-ttu-id="ad6fc-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>行動 **使用者裝置** (17) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Mobile User Device** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ad6fc-146">專用使用者裝置的範例為行動電話或在商店中透過無線電頻率進行通訊的條碼掃描器。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-146">An example of a dedicated user device is a mobile phone or a barcode scanner in a store that communicates via radio frequency.</span></span> <span data-ttu-id="ad6fc-147">這些系統在功能和可程式性方面都有很大的限制，且不會被視為「一般用途」的運算平臺。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-147">These systems are quite limited in functionality and programmability, and are not considered 'general purpose' computing platforms.</span></span> <span data-ttu-id="ad6fc-148">或者，也就是「一般用途」 (的行動系統範例，並不是專用的) 是一部掌上型的電腦。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-148">Alternately, an example of a mobile system that is 'general purpose' (i.e., is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="ad6fc-149">雖然在其可程式性方面有所限制，但可以下載新的軟體，並由使用者擴充其功能。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-149">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span>

</dd> <dt>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>

<span data-ttu-id="ad6fc-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**中繼器** (18) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>

<span data-ttu-id="ad6fc-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**橋接器/** 擴充項 (19) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Bridge/Extender** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>

<span data-ttu-id="ad6fc-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**閘道** (20) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Gateway** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>

<span data-ttu-id="ad6fc-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**儲存體 Virtualizer** (21) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Storage Virtualizer** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>

<span data-ttu-id="ad6fc-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Media Library** (22) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Media Library** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>

<span data-ttu-id="ad6fc-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>

<span data-ttu-id="ad6fc-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**NAS Head** (24) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**NAS Head** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>

<span data-ttu-id="ad6fc-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**獨立的 NAS** (25) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**Self-contained NAS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="UPS"></span><span id="ups"></span>

<span data-ttu-id="ad6fc-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>

<span data-ttu-id="ad6fc-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**IP 電話** (27) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**IP Phone** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>

<span data-ttu-id="ad6fc-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**管理控制器** (28) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Management Controller** (28)</span></span>


</dt> <dd>

<span data-ttu-id="ad6fc-161">此實例代表系統管理專用的專用硬體 (亦即基礎板管理控制器 (BMC) 或服務處理器) 。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-161">This instance represents specialized hardware dedicated to systems management (i.e., a Baseboard Management Controller (BMC) or service processor).</span></span>

<span data-ttu-id="ad6fc-162">「管理控制器」的管理範圍通常是包含它的單一受管理系統。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-162">The management scope of a "Management Controller" is typically a single managed system in which it is contained.</span></span>

</dd> <dt>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>

<span data-ttu-id="ad6fc-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**底座管理員** (29) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Chassis Manager** (29)</span></span>


</dt> <dd>

<span data-ttu-id="ad6fc-164">此實例代表專門用來管理 blade 底座和其包含裝置的系統。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-164">This instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="ad6fc-165">此值會用來代表貨架控制器。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-165">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="ad6fc-166">「底座管理員」是用於管理的匯總點，而且可能依賴從屬管理控制器來管理構成部分。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-166">A "Chassis Manager" is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span>

</dd> <dt>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>

<span data-ttu-id="ad6fc-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>以 **主機為基礎的 RAID 控制器** (30) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Host-based RAID controller** (30)</span></span>


</dt> <dd>

<span data-ttu-id="ad6fc-168">此實例代表主機電腦中包含的 RAID 存放控制器。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-168">This instance represents a RAID storage controller contained within a host computer.</span></span>

</dd> <dt>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>

<span data-ttu-id="ad6fc-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**儲存體裝置主機殼** (31) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Storage Device Enclosure** (31)</span></span>


</dt> <dd>

<span data-ttu-id="ad6fc-170">此實例代表包含存放裝置的主機殼。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-170">This instance represents an enclosure that contains storage devices.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="ad6fc-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (32) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="ad6fc-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**膝上型電腦** (33) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>

<span data-ttu-id="ad6fc-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**虛擬磁帶媒體** 櫃 (34) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Virtual Tape Library** (34)</span></span>


</dt> <dd>

<span data-ttu-id="ad6fc-174">虛擬程式庫系統的磁帶媒體櫃模擬。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-174">The emulation of a tape library by a Virtual Library System.</span></span>

</dd> <dt>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>

<span data-ttu-id="ad6fc-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**虛擬程式庫系統** (35) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Virtual Library System** (35)</span></span>


</dt> <dd>

<span data-ttu-id="ad6fc-176">使用磁片儲存體來模擬磁帶媒體櫃</span><span class="sxs-lookup"><span data-stu-id="ad6fc-176">Uses disk storage to emulate tape libraries</span></span>

</dd> <dt>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>

<span data-ttu-id="ad6fc-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**網路電腦/瘦用戶端** (36) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**Network PC/Thin Client** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>

<span data-ttu-id="ad6fc-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**FC 交換器** (37) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**FC Switch** (37)</span></span>


</dt> <dd>

<span data-ttu-id="ad6fc-179">專門用來切換第2層光纖通道框架。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-179">Dedicated to switching layer 2 fibre channel frames.</span></span>

</dd> <dt>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>

<span data-ttu-id="ad6fc-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Ethernet 交換器** (38) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Ethernet Switch** (38)</span></span>


</dt> <dd>

<span data-ttu-id="ad6fc-181">專門用來切換第2層乙太網路框架</span><span class="sxs-lookup"><span data-stu-id="ad6fc-181">Dedicated to switching layer 2 ethernet frames</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ad6fc-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ad6fc-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32568： 65535) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32568..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad6fc-184">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="ad6fc-184">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6fc-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ad6fc-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6fc-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad6fc-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6fc-187">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NameFormat" ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-187">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="ad6fc-188">電腦系統名稱的格式。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-188">The format of the computer system name.</span></span>

<dt>



 <span data-ttu-id="ad6fc-189"> ( "其他" ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-189">("Other")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-190"> ( "IP" ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-190">("IP")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-191"> ( 「撥號」 ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-191">("Dial")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-192"> ( "HID" ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-192">("HID")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-193"> ( "NWA" ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-193">("NWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-194"> ( "HWA" ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-194">("HWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-195"> ( 「X25」 ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-195">("X25")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-196"> ( "ISDN" ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-196">("ISDN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-197"> ( 「IPX」 ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-197">("IPX")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-198"> ( "DCC" ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-198">("DCC")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-199"> ( 「ICD」 ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-199">("ICD")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-200"> ( "E. 164" ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-200">("E.164")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-201"> ( 「SNA」 ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-201">("SNA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-202"> ( "OID/OSI" ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-202">("OID/OSI")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-203"> ( "WWN" ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-203">("WWN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6fc-204"> ( "NAA" ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-204">("NAA")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad6fc-205">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ad6fc-205">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6fc-206">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ad6fc-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ad6fc-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad6fc-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6fc-208">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (」**CIM \_**。**專用** 的 ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-208">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**Dedicated**")</span></span>
</dt> </dl>

<span data-ttu-id="ad6fc-209">描述當 **專用** 陣列包含值 2 (其他) 時，如何或為何專用系統。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-209">Describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="ad6fc-210">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ad6fc-210">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6fc-211">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ad6fc-211">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ad6fc-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad6fc-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6fc-213">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ PowerManagementCapabilities. PowerCapabilities" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統電源控制項 \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="ad6fc-213">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="ad6fc-214">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-214">This property is deprecated.</span></span> <span data-ttu-id="ad6fc-215">相反地，請使用 **CIM \_ PowerManagementCapabilitiesCIM \_ PowerManagementService** 類別中的 **PowerChangeCapabilities** 方法。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-215">Instead, use the **PowerChangeCapabilities** method in the **CIM\_PowerManagementCapabilitiesCIM\_PowerManagementService** class.</span></span>

<span data-ttu-id="ad6fc-216">已 **淘汰的描述：** 系統的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-216">**Deprecated description:** The power management capabilities of the system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ad6fc-217">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-217">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ad6fc-218">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-218">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ad6fc-219">**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-219">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ad6fc-220">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-220">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ad6fc-221">**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-221">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ad6fc-222">可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-222">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ad6fc-223">支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="ad6fc-223">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ad6fc-224">**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="ad6fc-224">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad6fc-225">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="ad6fc-225">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6fc-226">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ad6fc-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ad6fc-227">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad6fc-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6fc-228">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統硬體安全性 \| 001.4」 ) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="ad6fc-229">指出系統是否支援硬體重設作業。</span><span class="sxs-lookup"><span data-stu-id="ad6fc-229">Indicates whether the system supports the hardware reset operation.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ad6fc-230">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-230">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ad6fc-231">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-231">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ad6fc-232">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-232">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ad6fc-233">**已啟用** (4) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-233">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="ad6fc-234">**未執行** (5) </span><span class="sxs-lookup"><span data-stu-id="ad6fc-234">**Not Implemented** (5)</span></span>


<span data-ttu-id="ad6fc-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ad6fc-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ad6fc-236">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad6fc-236">Requirements</span></span>



| <span data-ttu-id="ad6fc-237">需求</span><span class="sxs-lookup"><span data-stu-id="ad6fc-237">Requirement</span></span> | <span data-ttu-id="ad6fc-238">值</span><span class="sxs-lookup"><span data-stu-id="ad6fc-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6fc-239">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad6fc-239">Minimum supported client</span></span><br/> | <span data-ttu-id="ad6fc-240">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ad6fc-240">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ad6fc-241">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad6fc-241">Minimum supported server</span></span><br/> | <span data-ttu-id="ad6fc-242">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad6fc-242">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ad6fc-243">命名空間</span><span class="sxs-lookup"><span data-stu-id="ad6fc-243">Namespace</span></span><br/>                | <span data-ttu-id="ad6fc-244">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="ad6fc-244">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ad6fc-245">MOF</span><span class="sxs-lookup"><span data-stu-id="ad6fc-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad6fc-246"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ad6fc-246"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad6fc-247">DLL</span><span class="sxs-lookup"><span data-stu-id="ad6fc-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad6fc-248"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ad6fc-248"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ad6fc-249">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad6fc-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad6fc-250">**CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="ad6fc-250">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

