---
title: EAP 的存取點初始化
description: 初始化時，AP (的存取點) 會查詢登錄中是否有安裝的驗證通訊協定。
ms.assetid: e230e01f-27df-4f61-8755-262ec11af660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185557c4b908780c09714aa9cc7fa4c80399812f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375332"
---
# <a name="access-point-initialization-of-eap"></a>EAP 的存取點初始化

初始化時，AP (的存取點) 會查詢登錄中是否有安裝的驗證通訊協定。 然後，AP 會針對每個驗證通訊協定呼叫匯出的函式 [**RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) 。 **RasEapGetInfo** 函式會接收 [**PPP \_ EAP \_ 資訊**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info)類型的單一參數。 AP 會使用此結構的 **dwEapTypeId** 成員來指定驗證通訊協定。 請注意，單一 DLL 可能支援一個以上的通訊協定。 如果 **RasEapGetInfo** 傳回任何 **不是 \_ 錯誤** 的值，AP 會假設驗證通訊協定無法使用。

從 [**RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) 返回時， [**PPP \_ EAP \_ 資訊**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info) 結構包含 eap DLL 中 [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85))、 [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))、 [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))和 [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) 函式的指標。 AP 服務會使用這些功能來與驗證通訊協定交互操作。 AP 會立即為每個驗證通訊協定呼叫 **RasEapInitialize** ，以將它初始化。 當服務關閉時，它會再次呼叫 **RasEapInitialize** ，這次會將 *fInitialize* 參數設定為 **FALSE** ，以指出驗證通訊協定應自行關閉。

 

 