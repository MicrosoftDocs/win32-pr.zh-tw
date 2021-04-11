---
description: TAPI 2.0 針對基本的 TAPI 1.4 功能提供少量的增強功能。
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34a3503916c6ec90c3a90e648ac3622c271d810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319147"
---
# <a name="tapi-20"></a>TAPI 2。0

TAPI 2.0 針對基本的 TAPI 1.4 功能提供少量的增強功能。 不過，有一些主要的架構變更大幅改善其穩定性。 大部分的變更都是將 TAPI 帶入 Windows NT 4.0 所需的基本變更，並充分利用其功能 (完整的32位支援、服務和 Unicode) 。 不過，這些變更是 TAPI 內部的變更，對 TAPI 應用程式的影響很小。

透過 Thunking 層支援 TAPI 1.3 和 1.4 (16 位應用程式的應用程式，) 在 Windows Server 2003 作業系統、Windows XP、Windows 2000 和 Windows NT 上運作正常。 不過，對服務提供者開發人員的影響相當重要。 這些作業系統的服務提供者必須是完全32位的 Unicode Dll，這些 Dll 可以在 TAPISRV 的內容中執行，而不是在 TAPI 應用程式的內容中， (與所有先前的 Win16 Tsp) 。 針對 TAPI 1.4 所設計的 Tsp 無法在 Windows Server 2003 作業系統、Windows XP、Windows 2000 或 Windows NT 上運作。

TAPI 2.0 也新增了「撥打電話中心」支援的重要功能，以及 (QOS) 支援的服務品質。

Windows 隨附的 TAPI 系統二進位檔支援所有應用程式的 TAPI 1.3 和1.4 版。 不過，16位應用程式不能使用 TAPI 2.0，而且您不能使用16位 TAPI 的 TSP。

 

 



