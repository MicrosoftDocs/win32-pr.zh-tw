---
description: 感應器管理員物件可存取可供您使用的感應器。
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: 感應器管理員物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715448a62c058c5e6825368003939e5ae2066847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112624"
---
# <a name="the-sensor-manager-object"></a>感應器管理員物件

感應器管理員物件可存取可供您使用的感應器。

若要使用感應器 API，您必須先呼叫 COM **CoCreateInstance** 方法來建立感應器管理員物件的實例，並取得其介面（名為 [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)）的指標。 感應器管理員會維護可用感應器的清單。 您可以使用 **ISensorManager** 來呼叫依類別或類型抓取感應器群組的方法，或者您也可以使用其唯一識別碼來呼叫方法，以取得特定感應器。 感應器管理員也可讓您註冊來接收事件，以在新感應器連線到平臺時通知您。

感應器管理員有時會提供感應器的指標，但使用者尚未啟用感應器。 例如，您通常可以在使用者啟用感應器之前，先取出非私用感應器屬性的值，例如感應器製造商或型號。 此資訊可協助您決定是否要要求使用者提供使用感應器的許可權。 您可以呼叫 [**ISensorManager：： RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) ，以提示使用者啟用特定感應器或感應器集合。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管理使用者權限](managing-user-permissions.md)
</dt> <dt>

[要求使用者權限](requesting-user-permissions.md)
</dt> </dl>

 

 
