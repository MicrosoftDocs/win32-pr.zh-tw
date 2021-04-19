---
description: 完成作業可讓應用程式指定當忙碌目的地之類的因素無法正常連接時，如何處理會話。
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: 完成會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971047"
---
# <a name="complete-a-session"></a>完成會話

完成作業可讓應用程式指定當忙碌目的地之類的因素無法正常連接時，如何處理會話。

[LINECALLCOMPLMODE \_ 常數](./linecallcomplmode--constants.md)會根據服務提供者的功能，定義應用程式可能會有的可能選項。

指定位址的多個呼叫完成要求可能在任何一次都未完成。 為了識別個別的要求，此實作為會傳回 [完成識別碼](completion-id-ovr.md)。 取消通話完成要求正在進行中，也會使用此呼叫完成識別碼。

**TAPI 2.x：** 請參閱 [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall)、 [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall)。

**TAPI 3.x：** 請參閱 [**ITBasicCallControl：： Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)、 [**ITBasicCallControl：:D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect)。

 

 
