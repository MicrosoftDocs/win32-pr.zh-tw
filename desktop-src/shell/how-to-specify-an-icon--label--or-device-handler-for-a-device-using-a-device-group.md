---
description: 裝置群組可針對宣告本身屬於該群組的任何裝置，允許其圖示、標籤或 DeviceHandlers 屬性的規格。
ms.assetid: 84433068-A869-479D-8ADA-E8221B38CCAE
title: 如何使用裝置群組來指定裝置的圖示、標籤或裝置處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e534aa6fa1bc7dbfe1bae3a2825a14f18096176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944184"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a>如何使用裝置群組來指定裝置的圖示、標籤或裝置處理常式

裝置群組可針對宣告本身屬於該群組的任何裝置，允許其圖示、標籤或 DeviceHandlers 屬性的規格。 如果裝置群組不是系統提供的裝置群組，則會在 **AutoplayHandlers** \\ **DeviceGroups** 金鑰下新增定義裝置群組的金鑰。 您不需要為每個群組設定三個屬性;您只能設定您想要自訂的屬性。 不過，裝置和裝置處理常式應該一律有相關聯的圖示和標籤，以符合最小的可用性需求。

## <a name="instructions"></a>指示


下列範例會使用具有數個連接之 Zip 磁片磁碟機的系統。 若未個別指定每個磁片磁碟機的圖示、標籤和 DeviceHandlers 值，您會建立名為 ZipDrive 的裝置群組，並在其中定義這些值。 接著，每個 Zip 磁片磁碟機會宣告為 ZipDrive 群組的成員。

首先，藉由新增下列 *ZipDrive* 索引鍵和其值來定義裝置群組。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceGroups
                        ZipDrive
                           Icons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-103
                           NoMediaIcons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-104
                           Label [REG_SZ] = My Custom Device Label
                           DeviceHandlers [REG_SZ] = MyDeviceHandler
```

接著會將每個 Zip 磁片磁碟機裝置宣告為 ZipDrive 群組的一部分，以繼承該群組的屬性。 在裝置實例的 **DeviceParameters** 索引鍵下，加入名為 DeviceGroup 的值，作為 **REG \_ SZ** 類型。 此值的資料輸入是裝置群組的名稱。

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceGroup [REG_SZ] = ZipDrive
```

您也可以在裝置群組的金鑰下新增圖示、標籤和 DeviceHandlers 以外的自訂裝置屬性，然後將其套用至屬於該裝置群組的所有裝置。

> [!Note]  
> 在裝置實例層級定義的屬性優先于在裝置群組層級定義的屬性，而這些屬性會優先于在裝置類別層級定義的屬性。

 

 

 



