---
title: 使用者驗證資訊
description: 用戶端電腦上的遠端存取連線管理員服務，會將使用者名稱和密碼傳送至遠端電腦上的 RAS 伺服器。
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f347cd9f42106619f2558bdcbc677c961b4fae749912c92dd32ac2c8096f6fd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127808"
---
# <a name="user-authentication-information"></a>使用者驗證資訊

用戶端電腦上的遠端存取連線管理員服務，會將使用者名稱和密碼傳送至遠端電腦上的 RAS 伺服器。 在建立連接之前，遠端伺服器會使用此資訊來驗證使用者。 根據預設，遠端存取連線管理員傳送目前登入之使用者的使用者名稱和密碼。 RAS 用戶端可以使用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)呼叫中指定的 [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85))結構，來指定不同的使用者名稱和密碼。

如果遠端伺服器無法以指定的資訊驗證使用者，則可以允許線上作業進入 [暫停狀態](paused-states.md) ，讓 RAS 用戶端向使用者收集不同的驗證資料。

 

 