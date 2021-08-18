---
description: 說明將裝置處理常式新增至裝置的程式。
title: 如何將裝置處理常式指派給裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de091a7206e8fe2d9ea2781e2c5b3475cb71446bae2effa9e017795ced8b9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092972"
---
# <a name="how-to-assign-a-device-handler-to-a-device"></a>如何將裝置處理常式指派給裝置

說明將裝置處理常式新增至裝置的程式。

## <a name="instructions"></a>指示


若要將裝置處理常式指派給裝置，請在裝置實例的 **裝置參數** 子機碼底下，新增名為 **DeviceHandlers** 的 **REG \_ SZ** 類型值。 此值的資料輸入是裝置處理常式的名稱。

以下是虛構的 Vid \_ 059&Pid 0031 裝置的範例專案 \_ 。

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

您也可以使用 [裝置群組](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) 或 [裝置類別](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) 設定來指派裝置處理常式。

 

 



