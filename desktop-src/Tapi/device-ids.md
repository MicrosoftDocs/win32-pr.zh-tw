---
description: 其他 TAPI 電話功能會使用開放電話裝置的控制碼來識別開啟的電話裝置。
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: 裝置識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970815"
---
# <a name="device-ids"></a>裝置識別碼

其他 TAPI 電話功能會使用開放電話裝置的控制碼來識別開啟的電話裝置。 使用電話裝置識別碼參數的電話裝置的唯一功能 (與電話控制碼) 的不同，是 [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) 和 [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) 函式。 應用程式可以使用 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) 函式搭配電話控制碼作為參數，來取得電話的裝置識別碼。

應用程式也可以藉由叫用 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)，取得與已開啟電話相關聯之各種裝置類別的裝置識別碼。 請參閱裝置類別名稱的 [TAPI 裝置類別](tapi-device-classes.md) 。

此函式會採用電話控制碼和裝置類別描述。 它會傳回與開啟的電話裝置相關聯之指定裝置類別之裝置的裝置識別碼。 如果裝置類別是「tapi/電話」，則會傳回電話裝置的裝置識別碼。

相較于行裝置（基本線路服務會提供對等的 POTS），不會為電話裝置定義最低保證的函式集合。 雖然每個電話裝置至少都提供本節所述的函式和訊息，但它們並不提供實體電話裝置上的任何實際操作。

 

 



