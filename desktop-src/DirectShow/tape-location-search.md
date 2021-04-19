---
description: 磁帶位置搜尋
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: 磁帶位置搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d1fb719f3b43374e5aa86f34c60e5b8f14d536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980601"
---
# <a name="tape-location-search"></a>磁帶位置搜尋

雖然 DV 裝置支援依時間碼或 (ATN) 的絕對軌編號來搜尋的命令，但是 MSDV 驅動程式並沒有可存取這些函式的標準、與裝置無關的方式。 唯一的選項是將未經處理的 AV/C 命令傳送到驅動程式，如 [發出原始的 av/c 命令](issuing-raw-av-c-commands.md)所述。

UVC 驅動程式支援磁帶位置搜尋的屬性集。 若要傳送搜尋命令，請使用 **IKsControl** 介面並設定 PROPSETID \_ EXT \_ TRANSPORT 屬性。 使用屬性集比將未經處理的 AV/C 命令傳送到裝置更安全，因為 AV/C 命令會略過篩選器並直接移至設備磁碟機。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制 DV 攝像機](controlling-a-dv-camcorder.md)
</dt> <dt>

[外部裝置傳輸屬性集](external-device-transport-property-set.md)
</dt> </dl>

 

 



