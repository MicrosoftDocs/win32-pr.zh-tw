---
description: 虛擬機器中的序列裝置包含序列控制器和序列埠。 每部虛擬機器只有一個串列控制器，且每個序列控制器都有兩個序列埠。
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: 序列裝置類別
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ae796b86837372d60bba83e51e0190b9c7d3f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987597"
---
# <a name="serial-devices-classes"></a><span data-ttu-id="101e4-104">序列裝置類別</span><span class="sxs-lookup"><span data-stu-id="101e4-104">Serial devices classes</span></span>

<span data-ttu-id="101e4-105">虛擬機器中的序列裝置包含序列控制器和序列埠。</span><span class="sxs-lookup"><span data-stu-id="101e4-105">The serial devices in a virtual machine consist of serial controllers and serial ports.</span></span> <span data-ttu-id="101e4-106">每部虛擬機器只有一個串列控制器，且每個序列控制器都有兩個序列埠。</span><span class="sxs-lookup"><span data-stu-id="101e4-106">Each virtual machine has exactly one serial controller, and each serial controller has exactly two serial ports.</span></span>

<span data-ttu-id="101e4-107">無法設定序列控制器的設定;因此，沒有相關聯的設定資料實例。</span><span class="sxs-lookup"><span data-stu-id="101e4-107">The settings for the serial controller are not configurable; therefore, there is no setting data instance associated with it.</span></span> <span data-ttu-id="101e4-108">此外，您無法在虛擬機器中新增或移除串列控制器或序列埠。</span><span class="sxs-lookup"><span data-stu-id="101e4-108">Also, you cannot add or remove serial controllers or serial ports from a virtual machine.</span></span> <span data-ttu-id="101e4-109">因此，沒有適用于序列裝置的資源集區實例。</span><span class="sxs-lookup"><span data-stu-id="101e4-109">Therefore, there are no resource pool instances for serial devices.</span></span>

<span data-ttu-id="101e4-110">以下是與序列裝置相關的虛擬化 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="101e4-110">The following are virtualization WMI classes related to serial devices.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="101e4-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="101e4-111">In this section</span></span>



| <span data-ttu-id="101e4-112">主題</span><span class="sxs-lookup"><span data-stu-id="101e4-112">Topic</span></span>                                                                                      | <span data-ttu-id="101e4-113">描述</span><span class="sxs-lookup"><span data-stu-id="101e4-113">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="101e4-114">**Msvm \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="101e4-114">**Msvm\_SerialController**</span></span>](msvm-serialcontroller.md)<br/>                         | <span data-ttu-id="101e4-115">代表序列控制器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="101e4-115">Represents the capabilities and management of the serial controller.</span></span><br/> |
| [<span data-ttu-id="101e4-116">**Msvm \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="101e4-116">**Msvm\_SerialPort**</span></span>](msvm-serialport.md)<br/>                                     | <span data-ttu-id="101e4-117">代表與序列控制器相關聯的序列埠。</span><span class="sxs-lookup"><span data-stu-id="101e4-117">Represents a serial port associated with the serial controller.</span></span><br/>      |
| [<span data-ttu-id="101e4-118">**Msvm \_ SerialPortOnSerialController**</span><span class="sxs-lookup"><span data-stu-id="101e4-118">**Msvm\_SerialPortOnSerialController**</span></span>](msvm-serialportonserialcontroller.md)<br/> | <span data-ttu-id="101e4-119">將序列埠與序列控制器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="101e4-119">Associates a serial port with a serial controller.</span></span><br/>                   |



 

 

 




