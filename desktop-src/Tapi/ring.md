---
description: 單一電話可能會以不同的響鈴模式環形。
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: 環形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d183c217447ca02bf5ee0c535360eecaea1f3c209cdb813ad58b77268f234d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773358"
---
# <a name="ring"></a>環形

單一電話可能會以不同的響鈴模式環形。 由於有各種不同的環形模式可用，因此環形模式會透過其響鈴模式號碼來識別。 環形模式數位的範圍從零到可用響鈴模式的數目減一。

應用程式用來控制電話裝置環形模式的函式是 [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring)，這會根據指定的響鈴模式來響鈴開啟的電話裝置，並使用 [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring)來傳回已開啟之手機裝置的目前響鈴模式。

當手機裝置的響鈴模式變更時，就會將 [**電話 \_ 狀態**](phone-state.md) 消息傳送至應用程式，以通知應用程式狀態變更。 此訊息的參數提供了變更的指示。

 

 



