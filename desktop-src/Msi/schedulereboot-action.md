---
description: 將 ScheduleReboot 動作插入動作順序，以提示使用者在安裝結束時重新開機系統。 使用 ForceReboot 動作，在安裝期間提示重新開機。
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: ScheduleReboot 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849330"
---
# <a name="schedulereboot-action"></a>ScheduleReboot 動作

將 ScheduleReboot 動作插入動作順序，以提示使用者在安裝結束時重新開機系統。 使用 [ForceReboot 動作](forcereboot-action.md) ，在安裝期間提示重新開機。

如果安裝具有使用者介面，安裝程式會在安裝結束時顯示訊息方塊和按鈕，詢問使用者是否想要重新開機系統。 使用者必須在完成安裝之前回應此提示。 如果安裝沒有使用者介面，系統會在結束時自動重新開機。

如果安裝程式判斷是否需要重新開機，它會自動提示使用者在安裝結束時重新開機，不論順序中是否有任何 ForceReboot 或 ScheduleReboot 動作。 例如，如果安裝程式需要取代任何在安裝期間使用的檔案，安裝程式會自動提示重新開機。

您可以藉由設定 [ [**重新開機**](reboot.md) ] 屬性，隱藏某些提示以重新開機。

如果 Windows Installer 在[多套件安裝](multiple-package-installations.md)期間遇到[ForceReboot](forcereboot-action.md)或 ScheduleReboot 動作，安裝程式將會停止並復原安裝。 您可以安裝屬於多套件安裝的其他套件，而這些套件不包含 ForceReboot 或 ScheduleReboot 動作。

## <a name="sequence-restrictions"></a>順序限制

沒有任何順序限制。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

例如，您可以在安裝需要重新開機的驅動程式之後，使用此動作來強制安裝程式提示重新開機。 如果安裝程式嘗試取代使用中的檔案，即使尚未使用 ScheduleReboot，它也會自動提示使用者重新開機。

ScheduleReboot 動作通常會放在序列的結尾，但可插入序列中的任何時間點。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[系統重新開機](system-reboots.md)
</dt> </dl>

 

 



