---
title: Newdev。h
description: 本節包含 Newdev 標頭的參考主題。
ms.assetid: 74195139-6899-4324-af77-d830c2642031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88efc393fdf192d55c8c5eeef513b56f2711996b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023656"
---
# <a name="newdevh"></a>Newdev。h

本節包含 Newdev 標頭的參考主題。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DiInstallDevice**](/windows/desktop/api/Newdev/nf-newdev-diinstalldevice)<br/>                                     | **DiInstallDevice** 函式會安裝指定的驅動程式，該驅動程式會預先安裝在系統中的指定裝置上的 [驅動程式存放區](/windows-hardware/drivers/install/driver-store)中。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**DiInstallDriver**](/windows/desktop/api/Newdev/nf-newdev-diinstalldrivera)<br/>                                     | **DiInstallDriver** 函式會在 [驅動程式存放區](/windows-hardware/drivers/install/driver-store)中預先安裝驅動程式，然後將驅動程式安裝在驅動程式所支援系統中的裝置上。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**DiRollbackDriver**](/windows/desktop/api/Newdev/nf-newdev-dirollbackdriver)<br/>                                   | **DiRollbackDriver** 函式會復原已安裝在指定裝置上的驅動程式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**DiShowUpdateDevice**](/windows/desktop/api/Newdev/nf-newdev-dishowupdatedevice)<br/>                               | **DiShowUpdateDevice** 函式會顯示指定裝置的硬體更新嚮導。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**DiUninstallDevice**](/windows/desktop/api/Newdev/nf-newdev-diuninstalldevice)<br/>                                 | [**DiUninstallDevice**](/windows/desktop/api/Newdev/nf-newdev-diuninstalldevice)函式會卸載裝置，並從系統中移除其裝置節點 ([devnode](/windows-hardware/drivers/)) 。 這不同于搭配使用 [**SetupDiCallClassInstaller**](/windows/desktop/api/Setupapi/nf-setupapi-setupdicallclassinstaller) 與 [**DIF \_ 移除**](/windows-hardware/drivers/install/dif-remove) 程式碼，因為它會嘗試卸載裝置節點，以及呼叫時出現的子 devnodes。<br/> 在 Windows 8 不會在呼叫時出現的任何子裝置將不會卸載。 不過，從 Windows 8 開始，在呼叫時不會出現的任何子裝置都會卸載。<br/> |
| [**UpdateDriverForPlugAndPlayDevices**](/windows/desktop/api/Newdev/nf-newdev-updatedriverforplugandplaydevicesa)<br/> | 如果有 INF 檔案和 [硬體識別碼](/windows-hardware/drivers/install/hardware-ids)， **UpdateDriverForPlugAndPlayDevices** 函式會針對符合硬體識別碼的裝置安裝更新的驅動程式。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

 

 

[將關於本主題的意見傳送給 Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Newdev.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "將關於本主題的意見傳送給 Microsoft")