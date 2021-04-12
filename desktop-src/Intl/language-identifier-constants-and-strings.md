---
description: 每個語言識別項都是由主要語言識別項所組成，指出語言和表示國家/地區的子語言識別項。
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: 語言識別項常數和字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80823e897a8325cbcb7207f91bde69397296767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319392"
---
# <a name="language-identifier-constants-and-strings"></a>語言識別項常數和字串

> [!IMPORTANT]
> 語言識別項常數已被取代，因此不建議使用。 最好是使用地區設定名稱，而非地區設定識別碼。

如需語言識別項的描述，請參閱 [語言識別項](language-identifiers.md) 。

主要或子語言識別項可以是使用者定義的或預先定義的識別碼。 如需預先定義的主要語言識別項及其有效的語言識別項，請參閱 [[MS-LCID]： Windows 語言代碼識別碼 (LCID) 參考](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f)。

> [!Note]  
> 如果沒有與主要語言識別項搭配使用的語言識別項，您的應用程式應該使用 **SUBLANG \_ 預設值**。 針對所有主要語言的 sublanguages，它應該使用 **SUBLANG \_ 中立** 的資源。

使用者定義的主要語言識別項具有範圍0x0200 至0x03ff 的值。 所有其他值則保留供作業系統使用。

使用者定義的子語言識別項具有範圍0x20 到0x3f 的值。 所有其他值則保留供作業系統使用。
