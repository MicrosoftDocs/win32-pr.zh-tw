---
description: 說明將裝置處理常式新增至裝置的程式。
title: 如何將裝置處理常式指派給裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16db6a39406e3d8ba7cd8b497e12883685b80d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973180"
---
# <a name="how-to-assign-a-device-handler-to-a-device"></a><span data-ttu-id="d3cb8-103">如何將裝置處理常式指派給裝置</span><span class="sxs-lookup"><span data-stu-id="d3cb8-103">How to Assign a Device Handler to a Device</span></span>

<span data-ttu-id="d3cb8-104">說明將裝置處理常式新增至裝置的程式。</span><span class="sxs-lookup"><span data-stu-id="d3cb8-104">Illustrates the process for adding a device handler to a device.</span></span>

## <a name="instructions"></a><span data-ttu-id="d3cb8-105">指示</span><span class="sxs-lookup"><span data-stu-id="d3cb8-105">Instructions</span></span>


<span data-ttu-id="d3cb8-106">若要將裝置處理常式指派給裝置，請在裝置實例的 **裝置參數** 子機碼底下，新增名為 **DeviceHandlers** 的 **REG \_ SZ** 類型值。</span><span class="sxs-lookup"><span data-stu-id="d3cb8-106">To assign a device handler to a device, under the **Device Parameters** subkey of the device instance, add a value of type **REG\_SZ** named **DeviceHandlers**.</span></span> <span data-ttu-id="d3cb8-107">此值的資料輸入是裝置處理常式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3cb8-107">The data entry for this value is the name of the device handler.</span></span>

<span data-ttu-id="d3cb8-108">以下是虛構的 Vid \_ 059&Pid 0031 裝置的範例專案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d3cb8-108">The following is an example entry for a fictitious Vid\_059&Pid\_0031 device.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceHandlers = MyDeviceHandler
```

<span data-ttu-id="d3cb8-109">您也可以使用 [裝置群組](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) 或 [裝置類別](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) 設定來指派裝置處理常式。</span><span class="sxs-lookup"><span data-stu-id="d3cb8-109">Device handlers can also be assigned by using [device group](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) or [device class](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) settings.</span></span>

 

 



