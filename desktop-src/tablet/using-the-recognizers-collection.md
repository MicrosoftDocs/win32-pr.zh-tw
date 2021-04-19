---
description: 如果您使用多個辨識器，您可以使用辨識器集合來列出可用的辨識器，並讓使用者從中進行選取。
ms.assetid: 1b89def0-3491-42da-9138-5280002e447a
title: 使用辨識器集合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d38625b3c6d4b8ed2475393ba45ae97b5bdc47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997487"
---
# <a name="using-the-recognizers-collection"></a>使用辨識器集合

如果您使用多個辨識器，您可以使用辨識 [**器集合來**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) 列出可用的辨識器，並讓使用者從中進行選取。 辨識器 **集合會** 檢查已安裝的辨識器、查詢辨識 [**器**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) 物件的屬性，並儲存結果。 應用程式可以使用辨識 **器集合來** 顯示可用的辨識器清單，而不需要載入每個辨識器 DLL。

> [!Note]  
> 辨識 [**器集合會**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) 使用系統登錄來檢查 Microsoft 辨識器和協力廠商辨識器。

 

下表顯示每個 Microsoft 辨識器所支援的語言識別項值。

> [!Note]  
> 沒有與 Microsoft 手勢辨識器相關聯的語言識別項。

 



| 辨識器名稱                                                      | 依序支援主要語言識別項、子語言識別項 ()                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft 手勢辨識器<br/>                              | 無<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Microsoft 英文 (英國) 手寫辨識器<br/> | LANG \_ 英文，SUBLANG \_ 英文 \_ UK<br/> LANG \_ 英文、SUBLANG \_ 英文 \_ EIRE<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Microsoft 英文 (美國) 手寫辨識器<br/>  | LANG \_ 英文、SUBLANG \_ 英文 \_<br/> LANG \_ 英文、SUBLANG \_ 英文 \_ AU<br/> LANG \_ 英文，SUBLANG \_ 英文 \_ 貝里斯<br/> LANG \_ 英文、SUBLANG \_ 英文 \_<br/> LANG \_ 英文、SUBLANG \_ 英文 \_ 加勒比海<br/> LANG \_ 英文、SUBLANG \_ 英文 \_ 牙買加<br/> LANG \_ 英文、SUBLANG \_ 英文 \_ NZ<br/> LANG \_ 英文、SUBLANG \_ 英文 \_ 菲律賓<br/> LANG \_ 英文、SUBLANG （ \_ 英文） \_ 南非 \_<br/> LANG \_ 英文、SUBLANG \_ 英文 \_ 特立尼達<br/> LANG \_ 英文、SUBLANG \_ 英文的 \_ 辛巴威<br/> LANG \_ 英文、SUBLANG \_ 中立<br/> |
| Microsoft 法文手寫辨識器<br/>                   | LANG \_ 法文、SUBLANG \_ 法文<br/> LANG \_ 法文、SUBLANG \_ 法文 \_ 比利時<br/> LANG \_ 法文、SUBLANG \_ 法文（ \_ 加拿大）<br/> LANG \_ 法文、SUBLANG \_ 法文 \_ 盧森堡<br/> LANG \_ 法文、SUBLANG \_ 法文 \_ 摩納哥<br/> LANG \_ 法文、SUBLANG \_ 法文 \_ 瑞士<br/> LANG \_ 法文、SUBLANG \_ 中立<br/>                                                                                                                                                                                                                                                                                     |
| Microsoft 德文手寫辨識器<br/>                   | LANG \_ 德文、SUBLANG \_ 德文<br/> LANG \_ 德文、SUBLANG \_ 德文 \_ 奧地利<br/> LANG \_ 德文、SUBLANG \_ 德文 \_ 列支敦斯登<br/> LANG \_ 德文、SUBLANG \_ 德文 \_ 盧森堡<br/> LANG \_ 德文、SUBLANG \_ 德文 \_ 瑞士<br/> LANG \_ 德文、SUBLANG \_ 中立<br/>                                                                                                                                                                                                                                                                                                                                |
| Microsoft 西班牙文手寫辨識器<br/>                  | LANG \_ 西班牙文，SUBLANG \_ 西班牙文<br/> LANG \_ 西班牙文，SUBLANG \_ 中立<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Microsoft 日文手寫辨識器<br/>                 | LANG \_ 日文、SUBLANG \_ 中性<br/> LANG \_ 日文、SUBLANG \_ 預設<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Microsoft 韓文手寫辨識器<br/>                   | LANG \_ 韓文、SUBLANG \_ 中立<br/> LANG \_ 韓文、SUBLANG \_ 預設<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Microsoft 中文 (簡化) 手寫辨識器<br/>     | LANG \_ 中文、SUBLANG \_ 簡體中文 \_<br/> LANG \_ 中文、SUBLANG \_ 中文 \_ 新加坡<br/> LANG \_ 中文、SUBLANG \_ 中性<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Microsoft 繁體中文 (繁體中文) 手寫辨識器<br/>    | LANG \_ 中文、SUBLANG \_ 繁體中文 \_<br/> LANG \_ 中文、SUBLANG \_ 中文 \_ HONGKONG<br/> LANG \_ 中文、SUBLANG \_ 中文 \_ 澳門<br/> LANG \_ 中文、SUBLANG \_ 中性<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

如需語言識別項的詳細資訊，請參閱 [語言識別項常數和字串](../intl/language-identifier-constants-and-strings.md)。

 

 
