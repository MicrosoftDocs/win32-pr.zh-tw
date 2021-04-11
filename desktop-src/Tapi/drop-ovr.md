---
description: 卸載或中斷會話的連線會終止通訊。 如果服務提供者支援，則應用程式可以選擇在中斷連接時傳送使用者的資訊。
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: 卸除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9bf3705d9b104b8816ce4b493ec6b188c5fe1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943312"
---
# <a name="drop"></a>卸除

卸載或中斷會話的連線會終止通訊。 如果服務提供者支援，則應用程式可以選擇在中斷連接時傳送使用者的資訊。

卸載會話的常見原因是使用者已要求中斷連線，或已捨棄會話的另一端。 當 TAPI 提供應用程式的會話時，也可以呼叫 drop 作業。 如果服務提供者支援這種情況，就會影響應用程式拒絕呼叫。

叫用卸載作業時，相關的會話有時也會受到影響。 例如，卸載會議電話可以捨棄所有個別的參與者。 狀態變更訊息會傳送至應用程式，以取得其狀態會受到影響的所有呼叫。

當有多個合作物件在呼叫時，會在不同的橋接或合作物件的設定中，捨棄作業可能不會實際清除呼叫。 例如，在橋接的情況下，呼叫可能不會被捨棄，因為來電中其他工作站的狀態可能會受到控制。 相反地，呼叫可以直接變更為非使用中狀態，而在其他工作站上保持連線。

在卸載作業之後，與會話相關聯的會話識別碼和大部分資源仍可供大部分的查詢作業使用。 當應用程式不再需要這些資源時，它必須 [終止會話](terminate-a-session-ovr.md) ，以避免記憶體流失。

**TAPI 2.x：** 請參閱 [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop)。

**TAPI 3.x：** 請參閱 [**ITBasicCallControl：:D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect)。

 

 
