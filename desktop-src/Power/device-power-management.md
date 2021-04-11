---
description: 裝置電源 API 可讓您輕鬆地判斷哪些裝置能夠從睡眠狀態喚醒系統，以及哪些睡眠狀態是這些裝置支援喚醒的裝置。 如需睡眠狀態的詳細資訊，請參閱系統電源狀態。
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: 裝置電源管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944242"
---
# <a name="device-power-management"></a>裝置電源管理

裝置電源 API 可讓您輕鬆地判斷哪些裝置能夠從睡眠狀態喚醒系統，以及哪些睡眠狀態是這些裝置支援喚醒的裝置。 如需睡眠狀態的詳細資訊，請參閱 [系統電源狀態](system-power-states.md)。

您可以使用 [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) 函式，在裝置清單中搜尋符合指定準則的裝置。 準則可能包括裝置支援系統狀態的能力，或從該狀態喚醒。 目前支援的旗標可在 WinNT 和 DevPower 中找到。

[**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate)函式會啟用或停用指定的裝置，使其無法從睡眠狀態喚醒系統。

裝置電源 API 可讓開發人員藉由提供使用者有關系統正在執行之工作的詳細資訊，以及對系統中的裝置進行更多的控制，來創造更好的使用者體驗。 裝置電源在電力耗用量很重要的情況下很有用，例如在以電池執行的可攜式裝置中。 例如，在桌上型電腦中使用的電源管理配置可能不是膝上型電腦的最佳配置，因此使用者可能會想要停用某些裝置，使其無法喚醒系統。 這可以節省能源，因為當系統處於睡眠模式時，已停用的裝置將不會繪製電源。

如需範例，請參閱 [使用裝置電源 API](using-the-device-power-api.md)。

 

 



