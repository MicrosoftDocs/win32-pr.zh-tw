---
description: 商務規則可讓應用程式在執行時間使用邏輯，以限定授與用戶端的許可權。
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: 商務規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195574"
---
# <a name="business-rules"></a>商務規則

商務規則可讓應用程式在執行時間使用邏輯，以限定授與用戶端的許可權。

商務規則是以 Visual Basic Scripting Edition (VBScript) 程式設計語言撰寫的腳本，或使用與 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) 物件相關聯的 Microsoft JScript 開發軟體撰寫的腳本。 當應用程式檢查作業的存取權時，授權管理員會先檢查目前的用戶端是否有權存取包含該作業但未與商務規則相關聯的任何工作。 如果未以此方式授與存取權，則授權管理員會執行與包含作業之任何工作相關聯的商務規則腳本。

應用程式會將資訊傳遞至商務規則腳本，作為一組代表參數名稱和值的陣列。 腳本會透過在腳本執行時所建立的 [**azbizrulecoNtext.businessruleresult**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) 物件來存取這些參數。

商務規則腳本無法指派給委派範圍所包含的工作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 c + + 中使用商務邏輯來限定存取權](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



