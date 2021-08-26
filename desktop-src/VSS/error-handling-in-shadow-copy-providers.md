---
description: VSS 允許有許多陰影複製存在一次，但它只允許在呼叫 >ivssbackupcomponents：： StartSnapshotSet 與從呼叫 >ivssbackupcomponents：:D oSnapshotSet 之間進行某個陰影複製集建立。
ms.assetid: 26657fc2-180f-4ebb-820c-2159e7fe7584
title: 陰影複製提供者中的錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0963df4c9c81c2cd9f96e7c1828243f3910a1df34d5ef94a714f17c57b404b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032678"
---
# <a name="error-handling-in-shadow-copy-providers"></a>陰影複製提供者中的錯誤處理

VSS 允許有許多陰影複製存在一次，但它只允許在呼叫 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) 與從呼叫 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)之間進行某個陰影複製集建立。

## <a name="no-partial-commit"></a>無部分認可

如果任何提供者無法在陰影複製集中的任何磁片區或 LUN 上進行陰影複製，則建立整個陰影複製集會失敗。 這是原廠設定。 這項設計可簡化與部分失敗語義相關聯的行為問題，並在集合中的所有陰影複製間維持一致的時間點。

## <a name="reporting-fault-conditions"></a>報告錯誤狀況

如果發生提供者錯誤或錯誤狀況，則提供者必須將錯誤記錄到應用程式事件記錄檔。 這包括（但不限於）在建立或匯入陰影複製集時的任何提供者特定錯誤，或在建立後寫入複製陰影複製的資源配置失敗。 當陰影複製組中的磁片區處於凍結狀態時，不一定會發生這項記錄。

## <a name="valid-provider-return-values"></a>有效的提供者傳回值

下表列出提供者方法的有效傳回碼及其意義。



| 值                                                                                                                                                                              | 描述                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span>S \_ 確定<br/>                                                                                                                     | 此方法成功。<br/>                                                                                                                                                                                                                  |
| <span id="E_OUTOFMEMORY"></span><span id="e_outofmemory"></span>E \_ OUTOFMEMORY<br/>                                                                                          | 提供者超出記憶體或其他系統資源。<br/>                                                                                                                                                                                    |
| <span id="E_INVALIDARG"></span><span id="e_invalidarg"></span>E \_ INVALIDARG<br/>                                                                                             | 其中一個參數值無效。<br/>                                                                                                                                                                                                   |
| <span id="E_ACCESSDENIED"></span><span id="e_accessdenied"></span>E \_ ACCESSDENIED<br/>                                                                                       | 非特殊許可權的用戶端已嘗試呼叫提供者。<br/>                                                                                                                                                                                |
| <span id="VSS_E_BAD_STATE"></span><span id="vss_e_bad_state"></span>VSS \_ E \_ 不良 \_ 狀態<br/>                                                                                  | 任何提供者都不支援要求的作業，或無法在物件上執行作業，因為物件不是處於正確的狀態。<br/>                                                                                     |
| <span id="VSS_E_OBJECT_NOT_FOUND"></span><span id="vss_e_object_not_found"></span>\_ \_ \_ \_ 找不到 VSS E 物件<br/>                                                            | 參數指的是找不到的物件 (例如陰影複製識別碼、陰影複製集識別碼或磁片區。 ) <br/>                                                                                                                               |
| <span id="VSS_E_INSUFFICIENT_STORAGE"></span><span id="vss_e_insufficient_storage"></span>VSS \_ E \_ \_ 儲存體不足<br/>                                                 | 提供者無法執行操作，因為磁碟空間不足。<br/>                                                                                                                                                           |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED"></span><span id="vss_e_volume_not_supported"></span>\_ \_ \_ 不支援 VSS E 磁片區 \_<br/>                                                | 這部電腦上沒有任何提供者支援磁片區上所要求的操作。<br/>                                                                                                                                                                |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED_BY_PROVIDER"></span><span id="vss_e_volume_not_supported_by_provider"></span>\_ \_ \_ \_ \_ 提供者不支援的 \_ VSS E 磁片區<br/>          | 提供者不支援磁片區。<br/>                                                                                                                                                                                                   |
| <span id="VSS_E_MAXIMUM_NUMBER_OF_SNAPSHOTS_REACHED"></span><span id="vss_e_maximum_number_of_snapshots_reached"></span>VSS \_ E \_ 已 \_ \_ \_ 達到快照集數目上限 \_<br/> | 提供者已達到可支援的陰影複製數目上限。<br/>                                                                                                                                                           |
| <span id="VSS_E_PROVIDER_VETO"></span><span id="vss_e_provider_veto"></span>VSS \_ E \_ 提供者 \_ 否決<br/>                                                                      | 提供者遇到未對應到另一個傳回值的內部執行階段錯誤。 提供者也必須將事件寫入應用程式事件記錄檔，以提供使用者如何解決此問題的資訊。<br/> |
| <span id="VSS_E_CANNOT_REVERT_DISKID"></span><span id="vss_e_cannot_revert_diskid"></span>VSS \_ E \_ 無法 \_ 還原 \_ DISKID<br/>                                                | 一或多個磁片的 MBR 簽名碼或 GPT 識別碼無法設定為要求的值。 查看應用程式事件記錄檔以取得詳細資訊。<br/>                                                                                            |



 

提供者不應嘗試傳回任何其他錯誤代碼。

如果提供者傳回的錯誤碼不是預期的 (例如： **\_ FALSE**、E failed、e 非 **預期 \_** 或 **e \_ ABORT**) ，則 VSS **\_ 會** 將事件寫入事件記錄檔，以提及提供者和失敗的方法，並將錯誤轉譯為 **VSS E 未預期的 \_ \_ \_ 提供者 \_ 錯誤**，然後再返回要求者。 [**IVssProviderCreateSnapshotSet：： AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots)或 [**IVssProviderNotifications：： OnUnload**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidernotifications-onunload)的任何傳回都不會進行這項操作。

 

 




