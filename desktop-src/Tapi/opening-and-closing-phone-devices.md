---
description: 在決定電話裝置的功能之後，應用程式必須先開啟裝置，才能存取該手機上的功能。
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: 開啟和關閉手機裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998465"
---
# <a name="opening-and-closing-phone-devices"></a>開啟和關閉手機裝置

在決定電話裝置的功能之後，應用程式必須先開啟裝置，才能存取該手機上的功能。 成功開啟手機裝置之後，應用程式會傳回代表開啟電話的控制碼。 您可以使用不同的模式開啟手機裝置，藉此提供共用電話裝置的結構化方式。

[**PhoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)函式會開啟指定的電話裝置，讓應用程式能夠存取電話上的功能。 電話裝置會透過裝置識別碼（以 *dwDeviceID* 參數傳遞）來識別 **phoneOpen** 。

 

 



