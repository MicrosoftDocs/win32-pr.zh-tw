---
description: 從 Windows Vista 開始，Windows 隨附的主控台專案會獲得可在 API 呼叫中使用的正式名稱，或是以程式設計方式啟動該專案的命令列指令。
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: 主控台專案的正式名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebf831bfb1cb86c41a8f97c2bfa041dad836e4b77f8fd233cb94d4a3951c38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943468"
---
# <a name="canonical-names-of-control-panel-items"></a>主控台專案的正式名稱

從 Windows Vista 開始，Windows 隨附的主控台專案會獲得可在 API 呼叫中使用的正式名稱，或是以程式設計方式啟動該專案的[命令列指令](executing-control-panel-items.md)。 從 Windows 7 和 Windows Server 2008 R2，正式名稱可在群組原則中用來隱藏特定的主控台專案。 本主題提供每個主控台專案的詳細資料：標準名稱、GUID、模組名稱，以及辨識正式名稱的作業系統版本。

> [!Note]  
> Windows Vista 之前，不支援主控台專案的正式名稱。

 

-   [主控台標準名稱](#control-panel-canonical-names)
-   [已淘汰主控台正式名稱](#deprecated-control-panel-canonical-names)
-   [在群組原則中使用正式名稱](#using-canonical-names-in-local-group-policy)
-   [備註](#remarks)

## <a name="control-panel-canonical-names"></a>主控台標準名稱

使用這些值時，請記住下列事項：

-   根據定義，標準名稱不會根據系統語言而變更;即使系統的語言不是，它們一律會是英文。
-   並非所有主控台專案都存在於各種 Windows 中。
-   只有在系統上偵測到正確的硬體時，才會顯示某些主控台專案。
-   協力廠商也可以新增主控台專案。 此處所列的正式名稱只適用于 Windows 隨附的主控台專案。

以下是 Windows 8.1 中可用的主控台專案：

-   [重要訊息中心](#action-center)
-   [系統管理工具](#administrative-tools)
-   [播放](#autoplay)
-   [生物特徵辨識裝置](#biometric-devices)
-   [BitLocker 磁碟機加密](#bitlocker-drive-encryption)
-   [色彩管理](#color-management)
-   [認證管理員](#credential-manager)
-   [日期及時間](#date-and-time)
-   [預設程式](#default-programs)
-   [裝置管理員](#device-manager)
-   [裝置和印表機](#devices-and-printers)
-   [顯示器](#display)
-   [輕鬆存取中心](#ease-of-access-center)
-   [家庭安全](#family-safety)
-   [檔案歷程記錄](#file-history)
-   [資料夾選項](#folder-options)
-   [字型](#fonts)
-   [HomeGroup](#homegroup)
-   [索引選項](#indexing-options)
-   [紅外線](#infrared)
-   [網際網路選項](#internet-options)
-   [iSCSI 啟動器](#iscsi-initiator)
-   [iSNS 伺服器](#isns-server)
-   [鍵盤](#keyboard)
-   [位置設定](#location-settings)
-   [滑鼠](#mouse)
-   [MPIOConfiguration](#mpioconfiguration)
-   [網路和共用中心](#network-and-sharing-center)
-   [通知區域圖示](#notification-area-icons)
-   [畫筆和觸控](#pen-and-touch)
-   [個人化](#personalization)
-   [電話和數據機](#phone-and-modem)
-   [電源選項](#power-options)
-   [[程式和功能]](#programs-and-features)
-   [復原](#recovery)
-   [區域](#region)
-   [RemoteApp 和桌面連線](#remoteapp-and-desktop-connections)
-   [音效](#sound)
-   [語音辨識](#speech-recognition)
-   [儲存空間](#storage-spaces)
-   [同步中心](#sync-center)
-   [系統](#system)
-   [Tablet PC 設定](#tablet-pc-settings)
-   [工作列和流覽](#taskbar-and-navigation)
-   [疑難排解](#troubleshooting)
-   [TSAppInstall](#tsappinstall)
-   [使用者帳戶](#user-accounts)
-   [Windows Anytime Upgrade](#windows-anytime-upgrade)
-   [Windows Defender](#windows-defender)
-   [Windows 防火牆](#windows-firewall)
-   [Windows 行動中心](#windows-mobility-center)
-   [Windows To Go](#windows-to-go)
-   [Windows Update](#windows-update)
-   [工作資料夾](#work-folders)

### <a name="action-center"></a>控制中心

-   正式 **名稱**： Microsoft. ActionCenter
-   **GUID**： {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\ActionCenterCPL.dll，-1
-   **頁面**

    | 頁面名稱           | 開啟                      |
    |---------------------|----------------------------|
    | MaintenanceSettings | 自動維護      |
    | pageProblems        | 問題報告            |
    | pageReliabilityView | 可靠性監視器        |
    | pageResponseArchive | 封存的訊息          |
    | pageSettings        | 問題報告設定 |

    

     

### <a name="administrative-tools"></a>[系統管理工具]

-   正式 **名稱**： Microsoft. 依次
-   **GUID**： {D20EA4E1-3957-11d2-A40B-0C5020524153}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ system32 \\shell32.dll，-22982

### <a name="autoplay"></a>自動播放

-   正式 **名稱**： Microsoft. 自動播放
-   **GUID**： {9C60DE1E-E5FC-40f4-A487-460851A8D915}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\autoplay.dll，-1

### <a name="biometric-devices"></a>生物特徵辨識裝置

-   正式 **名稱**： Microsoft. BiometricDevices
-   **GUID**： {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\biocpl.dll，-1

### <a name="bitlocker-drive-encryption"></a>BitLocker 磁碟機加密

-   正式 **名稱**： Microsoft. microsoft.bitlockerdriveencryption
-   **GUID**： {D9EF8727-CAC2-4e60-809E-86F80A666C91}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\fvecpl.dll，-1

### <a name="color-management"></a>色彩管理

-   正式 **名稱**： Microsoft. ColorManagement
-   **GUID**： {B2C761C6-29BC-4f19-9251-E6195265BAF1}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% systemroot% \\ system32 \\colorcpl.exe，-6

### <a name="credential-manager"></a>認證管理員

-   正式 **名稱**： Microsoft. CredentialManager
-   **GUID**： {1206F5F1-0569-412C-8FEC-3204630DFB70}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ system32 \\Vault.dll，-1
-   **頁面**

    | 頁面名稱                   | 開啟               |
    |-----------------------------|---------------------|
    | ?SelectedVault = CredmanVault | Windows 認證 |

    

     

### <a name="date-and-time"></a>日期及時間

-   正式 **名稱**： Microsoft. >formatting.dateandtime.custom
-   **GUID**： {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\timedate.cpl，-51
-   **頁面**

    | 頁面名稱 | 開啟             |
    |-----------|-------------------|
    | 1         | 其他時鐘 |

    

     

### <a name="default-programs"></a>預設程式

-   正式 **名稱**： Microsoft. DefaultPrograms
-   **GUID**： {17cd9488-1228-4b2f-88ce-4298e93e0966}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\sud.dll，-1
-   **頁面**

    | 頁面名稱          | 開啟                |
    |--------------------|----------------------|
    | pageDefaultProgram | 設定預設程式 |
    | pageFileAssoc      | 設定關聯     |

    

     

### <a name="device-manager"></a>裝置管理員

-   正式 **名稱**： Microsoft. DeviceManager
-   **GUID**： {74246bfc-4c96-11d0-abef-0020af6b0b7a}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\devmgr.dll，-4

### <a name="devices-and-printers"></a>[裝置和印表機]

-   正式 **名稱**： Microsoft. DevicesAndPrinters
-   **GUID**： {A8A91A66-3A7D-4424-8D24-04E180695C7A}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% systemroot% \\ system32 \\DeviceCenter.dll，-1000

### <a name="display"></a>顯示

-   正式 **名稱**： Microsoft. Display
-   **GUID**： {C555438B-3C23-4769-A71F-B6D3D9B6053A}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\Display.dll，-1
-   **頁面**

    | 頁面名稱 | 開啟             |
    |-----------|-------------------|
    | 設定  | 螢幕解析度 |

    

     

### <a name="ease-of-access-center"></a>輕鬆存取中心

-   正式 **名稱**： Microsoft. EaseOfAccessCenter
-   **GUID**： {D555645E-D4F8-4c29-A827-D93C859C4F2A}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\accessibilitycpl.dll，-10
-   **頁面**

    | 頁面名稱               | 開啟                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | pageEasierToClick       | 讓滑鼠更容易使用                                        |
    | pageEasierToSee         | 讓電腦看得更清楚                                     |
    | pageEasierWithSounds    | 使用文字或視覺效果替代音效                          |
    | pageFilterKeysSettings  | 設定篩選金鑰                                                  |
    | pageKeyboardEasierToUse | 讓鍵盤更容易使用                                     |
    | pageNoMouseOrKeyboard   | 不透過滑鼠或鍵盤來使用電腦                        |
    | pageNoVisual            | 不透過顯示器來使用電腦                                  |
    | pageQuestionsCognitive  | 取得建議，讓您的電腦更容易使用 (認知)  |
    | pageQuestionsEyesight   | 取得建議，讓您的電腦更容易使用 (視力)   |

    

     

### <a name="family-safety"></a>家庭安全

-   正式 **名稱**： Microsoft. ParentalControls
-   **GUID**： {96AE8D84-A250-4520-95A5-A47A7E3C548B}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\wpccpl.dll，-100
-   **頁面**

    | 頁面名稱   | 開啟                                  |
    |-------------|----------------------------------------|
    | pageUserHub | 選擇使用者並設定家庭安全 |

    

     

### <a name="file-history"></a>檔案歷程記錄

-   正式 **名稱**： Microsoft. FileHistory
-   **GUID**： {F6B6E965-E9B2-444B-9286-10C9152EDBC5}
-   **支援的 OS**： Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\fhcpl.dll，-52
-   檔案歷程記錄包含較新版本的備份和還原專案，但較舊的專案的正式名稱不會重新對應到檔案歷程記錄。

### <a name="folder-options"></a>資料夾選項

-   正式 **名稱**： Microsoft. FolderOptions
-   **GUID**： {6DFD7C5C-2451-11d3-A299-00C04F8EF6AF}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ system32 \\shell32.dll，-22985

### <a name="fonts"></a>字型

-   正式 **名稱**： Microsoft 字型
-   **GUID**： {93412589-74D4-4E4E-AD0E-E0CB621440FD}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\FontExt.dll，-8007

### <a name="homegroup"></a>HomeGroup

-   正式 **名稱**： Microsoft. 家庭
-   **GUID**： {67CA7650-96E6-4FDD-BB43-A8E774F73A57}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\hgcpl.dll，-1

### <a name="indexing-options"></a>索引編製選項

-   正式 **名稱**： Microsoft. IndexingOptions
-   **GUID**： {87D66A43-7B11-4A28-9811-C86EE395ACF7}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\srchadmin.dll，-601

### <a name="infrared"></a>紅外線

-   正式 **名稱**： Microsoft 紅外線
-   **GUID**： {A0275511-0E86-4ECA-97C2-ECD8F1221D08}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\irprops.cpl，-1

### <a name="internet-options"></a>網際網路選項

-   正式 **名稱**： Microsoft. InternetOptions
-   **GUID**： {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @C: \\ Windows \\ System32 \\inetcpl.cpl，-4312
-   **頁面**

    | 頁面名稱 | 開啟       |
    |-----------|-------------|
    | 1         | 安全性    |
    | 2         | 隱私權     |
    | 3         | Content     |
    | 4         | 連接 |
    | 5         | 程式    |
    | 6         | 進階    |

    

     

### <a name="iscsi-initiator"></a>iSCSI 啟動器

-   正式 **名稱**： Microsoft. iSCSIInitiator
-   **GUID**： {A304259D-52B8-4526-8B1A-A1D6CECC8243}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\iscsicpl.dll，-5001

### <a name="isns-server"></a>iSNS 伺服器

-   正式 **名稱**： Microsoft. iSNSServer
-   **GUID**： {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\isnssrv.dll，-5005
-   只有在 Windows 的伺服器版本中才會看到此主控台專案。

### <a name="keyboard"></a>鍵盤

-   正式 **名稱**： Microsoft. 鍵盤
-   **GUID**： {725BE8F7-668E-4C7B-8F90-46BDB0936430}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\main.cpl，-102

### <a name="location-settings"></a>位置設定

-   正式 **名稱**： Microsoft. LocationSettings
-   **GUID**： {E9950154-C418-419e-A90A-20C5287AE24B}
-   **支援的 OS**： Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\SensorsCpl.dll，-1

### <a name="mouse"></a>滑鼠

-   正式 **名稱**： Microsoft. 滑鼠
-   **GUID**： {6C8EEC18-8D75-41B2-A177-8831D59D2D50}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\main.cpl，-100
-   **頁面**

    | 頁面名稱 | 開啟           |
    |-----------|-----------------|
    | 1         | 指標        |
    | 2         | 指標選項 |
    | 3         | Wheel           |
    | 4         | 硬體        |

    

     

### <a name="mpioconfiguration"></a>MPIOConfiguration

-   正式 **名稱**： Microsoft. MPIOConfiguration
-   **GUID**： {AB3BE6AA-7561-4838-AB77-ACF8427DF426}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\mpiocpl.dll，-1000
-   只有在 Windows 的伺服器版本中才會看到此主控台專案。

### <a name="network-and-sharing-center"></a>網路和共用中心

-   正式 **名稱**： Microsoft. NetworkAndSharingCenter
-   **GUID**： {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\netcenter.dll，-1
-   **頁面**

    | 頁面名稱  | 開啟                     |
    |------------|---------------------------|
    | 進階   | Advanced 共用設定 |
    | ShareMedia | 媒體串流選項   |

    

     

### <a name="notification-area-icons"></a>通知區域圖示

-   正式 **名稱**： Microsoft. NotificationAreaIcons
-   **GUID**： {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\taskbarcpl.dll，-1

### <a name="pen-and-touch"></a>畫筆和觸控

-   正式 **名稱**： Microsoft. PenAndTouch
-   **GUID**： {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\tabletpc.cpl，-10103
-   **頁面**

    | 頁面名稱 | 開啟       |
    |-----------|-------------|
    | 1         | 筆觸      |
    | 2         | Handwriting |

    

     

### <a name="personalization"></a>個人化

-   正式 **名稱**： Microsoft 個人化
-   **GUID**： {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\themecpl.dll，-1
-   **頁面**

    | 頁面名稱        | 開啟                |
    |------------------|----------------------|
    | pageColorization | 色彩和外觀 |
    | pageWallpaper    | 桌面背景   |

    

     

### <a name="phone-and-modem"></a>電話和數據機

-   正式 **名稱**： Microsoft. PhoneAndModem
-   **GUID**： {40419485-C444-4567-851A-2DD7BFA1684D}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\telephon.cpl，-1
-   此值啟動的視窗在 Windows 8 之前的 Windows 版本中的標題為「位置資訊」。 當 Windows 8 時，專案的 UI 會大幅變更。

### <a name="power-options"></a>電源選項

-   正式 **名稱**： Microsoft. PowerOptions
-   **GUID**： {025A5937-A6BE-4686-A844-36FE4BEC8B6D}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\powercpl.dll，-1
-   **頁面**

    | 頁面名稱          | 開啟              |
    |--------------------|--------------------|
    | pageGlobalSettings | 系統設定    |
    | pagePlanSettings   | 編輯計畫設定 |

    

     

### <a name="programs-and-features"></a>[程式和功能]

-   正式 **名稱**： Microsoft. ProgramsAndFeatures
-   **GUID**： {7b81be6a-ce2b-4676-a29e-eb907a5126c5}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% systemroot% \\ system32 \\appwiz.cpl，-159
-   **頁面**

    | 頁面名稱                                | 開啟             |
    |------------------------------------------|-------------------|
    | ::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD} | 已安裝的更新 |

    

     

### <a name="recovery"></a>復原

-   正式 **名稱**： Microsoft. Recovery
-   **GUID**： {9FE63AFD-59CF-4419-9775-ABCC3849F861}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\recovery.dll，-101

### <a name="region"></a>區域

-   正式 **名稱**： Microsoft. RegionAndLanguage
-   **GUID**： {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\intl.cpl，-1
-   在 Windows 7 中找到的地區和語言專案是依 Windows 8 分割。 RegionAndLanguage 現在會啟動區域專案。 若要啟動語言專案，請使用 [Microsoft language](#location-settings)。
-   **頁面**

    | 頁面名稱 | 開啟          |
    |-----------|----------------|
    | 1         | 位置       |
    | 2         | 系統管理 |

    

     

### <a name="remoteapp-and-desktop-connections"></a>RemoteApp 和桌面連線

-   正式 **名稱**： Microsoft. RemoteAppAndDesktopConnections
-   **GUID**： {241D7C96-F8BF-4F85-B01F-E2B043341A4B}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\tsworkspace.dll，-15300

### <a name="sound"></a>音效

-   正式 **名稱**： Microsoft. 音效
-   **GUID**： {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\mmsys.cpl，-300

### <a name="speech-recognition"></a>語音辨識

-   正式 **名稱**： Microsoft. SpeechRecognition
-   **GUID**： {58E3C745-D971-4081-9034-86E34B30836A}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\ 語音 \\ SpeechUX \\speechuxcpl.dll，-1

### <a name="storage-spaces"></a>儲存空間

-   正式 **名稱**： Microsoft. StorageSpaces
-   **GUID**： {F942C606-0914-47AB-BE56-1321B8035096}
-   **支援的 OS**： Windows 8、Windows 8。1
-   **模組名稱**： @C: \\ Windows \\ System32 \\SpaceControl.dll，-1

### <a name="sync-center"></a>同步中心

-   正式 **名稱**： Microsoft. SyncCenter
-   **GUID**： {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\SyncCenter.dll，-3000

### <a name="system"></a>系統

-   正式 **名稱**： Microsoft.System
-   **GUID**： {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\systemcpl.dll，-1

### <a name="tablet-pc-settings"></a>Tablet PC 設定

-   正式 **名稱**： Microsoft. TabletPCSettings
-   **GUID**： {80F3F1D5-FECA-45F3-BC32-752C152E456E}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\tabletpc.cpl，-10100

### <a name="taskbar-and-navigation"></a>工作列和流覽

-   正式 **名稱**： Microsoft. 工作列
-   **GUID**： {0DF44EAA-FF21-4412-828E-260A8728E7F1}
-   **支援的 OS**： Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ system32 \\shell32.dll，-32517

### <a name="troubleshooting"></a>疑難排解

-   正式 **名稱**： Microsoft. 疑難排解
-   **GUID**： {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\DiagCpl.dll，-1
-   **頁面**

    | 頁面名稱   | 開啟   |
    |-------------|---------|
    | HistoryPage | 記錄 |

    

     

### <a name="tsappinstall"></a>TSAppInstall

-   正式 **名稱**： Microsoft. TSAppInstall
-   **GUID**： {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}
-   **支援的 OS**： Windows 7、Windows 8 Windows 8。1
-   **模組名稱**： @% systemroot% \\ system32 \\tsappinstall.exe，-2001

### <a name="user-accounts"></a>使用者帳戶

-   正式 **名稱**： Microsoft. UserAccounts
-   **GUID**： {60632754-c523-4b62-b45c-4172da012619}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\usercpl.dll，-1

### <a name="windows-anytime-upgrade"></a>Windows Anytime Upgrade

-   正式 **名稱**： Microsoft. WindowsAnytimeUpgrade
-   **GUID**： {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @ $ (resourceString。 \_SYS \_ MOD \_ 路徑) ，-1

### <a name="windows-defender"></a>Windows Defender

-   正式 **名稱**： Microsoft. windowsdefender.msi
-   **GUID**： {D8559EB9-20C0-410E-BEDA-7ED416AECC2A}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% ProgramFiles% \\ Windows Defender \\MsMpRes.dll，-104

### <a name="windows-firewall"></a>Windows 防火牆

-   正式 **名稱**： Microsoft. windows 防火牆
-   **GUID**： {4026492F-2F69-46B8-B9BF-5654FC07E423}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @C: \\ Windows \\ system32 \\FirewallControlPanel.dll，-12122
-   **頁面**

    | 頁面名稱         | 開啟        |
    |-------------------|--------------|
    | pageConfigureApps | 允許的應用程式 |

    

     

### <a name="windows-mobility-center"></a>Windows 行動中心

-   正式 **名稱**： Microsoft. MobilityCenter
-   **GUID**： {5ea4f148-308c-46d7-98a9-49041b1dd468}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ system32 \\mblctr.exe，-1002

### <a name="windows-to-go"></a>Windows To Go

-   正式 **名稱**： Microsoft. PortableWorkspaceCreator
-   **GUID**： {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}
-   **支援的 OS**： Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ System32 \\pwcreator.exe，-151

### <a name="windows-update"></a>Windows Update

-   正式 **名稱**： Microsoft. windowsupdate.log
-   **GUID**： {36eef7db-88ad-4e81-ad49-0e313f0c35f8}
-   **支援的 OS**： Windows Vista、Windows 7、Windows 8、Windows 8。1
-   **模組名稱**： @% SystemRoot% \\ system32 \\wucltux.dll，-1
-   **頁面**

    | 頁面名稱         | 開啟               |
    |-------------------|---------------------|
    | pageSettings      | 變更設定     |
    | pageUpdateHistory | 查看更新歷程記錄 |

    

     

### <a name="work-folders"></a>工作資料夾

-   正式 **名稱**： Microsoft. workfolders.domainname
-   **GUID**： {ECDB0924-4208-451E-8EE0-373C0956DE16}
-   **支援的 OS**： Windows 8。1
-   **模組名稱**： @C: \\ Windows \\ System32 \\WorkfoldersControl.dll，-1

## <a name="deprecated-control-panel-canonical-names"></a>已淘汰主控台正式名稱

以下是 Windows 8.1 或更新版本不再使用的標準名稱。 部分已完全移除。 在這些情況下，其他專案已重新對應：

-   主控台專案已重新命名。 重新命名的專案會獲得新的正式名稱，但會保留相同的 GUID。 在此情況下，舊的正式名稱會啟動重新命名的主控台專案。 請注意，啟動的專案可能不會使用與該專案較舊版本相同的 UI。
-   一或多個主控台專案的功能會移動或合併到新的專案中。 在此情況下，舊的正式名稱會對應至最適當的新主控台專案。

> [!Note]  
> 重新對應存在以提供回溯相容性。 您不應該在新的程式碼中使用已被取代的值。

 



| 已淘汰的正式名稱                                   | 主控台專案                | GUID                                   | 備註                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddHardware                                       | 新增硬體                      | {7A979262-40CE-46ff-AEEE-7884AC3B6136} | 從 Windows 7 地圖[DevicesAndPrinters 至 Microsoft。](#devices-and-printers)                                                                                                                                                                                                                                                                            |
| AudioDevicesAndSoundThemes                        | 音效                             | {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D} | 地圖到[Microsoft](#sound) ，從 Windows 7 到的音效。                                                                                                                                                                                                                                                                                                        |
| BackupAndRestoreCenter/Microsoft. BackupAndRestore | 備份及還原中心         | {B98A2BEA-7D42-4558-8BD1-832F41BAC6FD} | BackupAndRestoreCenter 會對應到 microsoft. BackupAndRestore Windows 7。 從 Windows 8 移除兩者;請改用[FileHistory](#file-history) 。                                                                                                                                                                                   |
| Microsoft CardSpace                                         | Windows CardSpace                 | {78CB147A-98EA-4AA6-B0DF-C8681F69341C} | 從 Windows 8 移除。                                                                                                                                                                                                                                                                                                                                  |
| DesktopGadgets                                    | 桌面小工具                   | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | 從 Windows 8 移除。                                                                                                                                                                                                                                                                                                                                  |
| GetProgramsOnline                                 | Windows 交易市集               | {3e7efb4c-faf1-453d-89eb-56026875ef90} | 從 Windows 7 移除。                                                                                                                                                                                                                                                                                                                                  |
| InfraredOptions                                   | 紅外線                          | {A0275511-0E86-4ECA-97C2-ECD8F1221D08} | 從 Windows 7 地圖到[Microsoft. 紅外線](#infrared)。                                                                                                                                                                                                                                                                                                  |
| Microsoft. Language                                          | 語言                          | {BF782CC9-5A52-4A17-806C-2A894FFEEAC5} | 從 Windows 10 1803 版移除                                                                                                                                                                                                                                                                                                                    |
| LocationAndOtherSensors                           | 定位和其他感應器        | {E9950154-C418-419e-A90A-20C5287AE24B} | 從 Windows 8 地圖[LocationSettings](#infrared) 。                                                                                                                                                                                                                                                                                          |
| PenAndInputDevices                                | 畫筆和輸入裝置             | {F82DF8F7-8B9F-442E-A48C-818EA735FF9B} | 從 Windows 7 地圖[PenAndTouch 至 Microsoft。](#pen-and-touch)                                                                                                                                                                                                                                                                                          |
| PeopleNearMe                                      | 近端分享                    | {5224F545-A443-4859-BA23-7B5A95BDC8EF} | 從 Windows 8 移除。                                                                                                                                                                                                                                                                                                                                  |
| PerformanceInformationAndTools                    | 效能資訊和工具 | {78F3955E-3B90-4184-BD14-5397C15F1EFC} | 從 Windows 8.1 移除。                                                                                                                                                                                                                                                                                                                                |
| PhoneAndModemOptions                              | 電話和數據機                   | {40419485-C444-4567-851A-2DD7BFA1684D} | 從 Windows 7 地圖[PhoneAndModem 至 Microsoft。](#phone-and-modem)                                                                                                                                                                                                                                                                                      |
| Microsoft 印表機                                          | 印表機                          | {2227A280-3AEA-1069-A2DE-08002B30309D} | 從 Windows 7 地圖[DevicesAndPrinters 至 Microsoft。](#devices-and-printers)                                                                                                                                                                                                                                                                            |
| ProblemReportsAndSolutions                        | 問題報告與解決方案     | {FCFEECAE-EE1B-4849-AE50-685DCF7717EC} | 從 Windows 7 地圖[ActionCenter 至 Microsoft。](#action-center)                                                                                                                                                                                                                                                                                         |
| RegionalAndLanguageOptions                        | 地區及語言選項     | {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0} | 從 Windows 7 地圖[RegionAndLanguage 至 Microsoft。](#region) 請注意，從 Windows 8，區域和語言都有各自的主控台專案。 RegionalAndLanguageOptions 和 Microsoft RegionAndLanguage 目前都會開啟區域專案。 您必須使用 [Microsoft 語言](#location-settings) 來存取語言專案。 |
| SecurityCenter                                    | Windows 資訊安全中心           | {087DA31B-0DD3-4537-8E23-64A18591F88B} | 從 Windows 7 地圖[ActionCenter 至 Microsoft。](#action-center)                                                                                                                                                                                                                                                                                         |
| SpeechRecognitionOptions                          | 語音辨識選項        | {58E3C745-D971-4081-9034-86E34B30836A} | 從 Windows 7 地圖[SpeechRecognition 至 Microsoft。](#speech-recognition)                                                                                                                                                                                                                                                                               |
| TaskbarAndStartMenu                               | 工作列和 [開始] 功能表            | {0DF44EAA-FF21-4412-828E-260A8728E7F1} | 從 Windows 8 地圖到[Microsoft. 工作列](#speech-recognition)。                                                                                                                                                                                                                                                                                         |
| WelcomeCenter                                     | 迎賓中心                    | {CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1} | 地圖 Windows 7 中的 GettingStarted。 從 Windows 8 啟動主控台首頁。                                                                                                                                                                                                                                                      |
| WindowsSidebarProperties                          | Windows提要欄位屬性        | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | 地圖 Windows 7 中的 DesktopGadgets。 從 Windows 8 移除。                                                                                                                                                                                                                                                                                   |
| WindowsSideShow                                   | Windows SideShow                  | {E95A4861-D57A-4be1-AD0F-35267E261739} | Windows 8 中已淘汰的功能，已從 Windows 8.1 移除。                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a>使用本機群組原則中的正式名稱

從 Windows 7，您可以使用標準名稱，透過群組原則來限制對個別主控台專案的存取。 您可以在 Windows Vista 中使用相同的程式，但您必須使用模組名稱，而不是正式名稱。

### <a name="hiding-individual-control-panel-items"></a>隱藏個別主控台專案

如果您想要顯示比您想要隱藏更多主控台專案，請使用這個方法。

1.  執行 Gpedit.msc 檔案以啟動本機群組原則編輯器。 您也可以在 Windows 8.1 開始畫面中輸入「群組原則」，然後從搜尋結果中選取 [**編輯群組原則**]。
2.  選取 [**使用者** 設定]  >  **系統管理範本**  >  **主控台**。
3.  選取 [ **隱藏指定的主控台專案**]。
4.  在 [ **隱藏開啟的指定主控台專案** ] 視窗中，按一下 [ **已啟用**]。
5.  按一下 [選項] 面板中的 [ **顯示** ] 按鈕，以顯示不允許的主控台專案清單。
6.  在開啟的 [ **顯示內容** ] 視窗中，于 [ **值** ] 資料行中輸入正式名稱。 請依需要重複步驟。
7.  按一下 [確定]。

### <a name="showing-individual-control-panel-items"></a>顯示個別主控台專案

如果您想要隱藏超過您要顯示的主控台專案，請使用這個方法。

1.  執行 Gpedit.msc 檔案以啟動本機群組原則編輯器。 您也可以在 Windows 8.1 開始畫面中輸入「群組原則」，然後從搜尋結果中選取 [**編輯群組原則**]。
2.  選取 [**使用者** 設定]  >  **系統管理範本**  >  **主控台**。
3.  選取 [ **只顯示指定的主控台專案**]。
4.  在 [ **只顯示開啟的指定主控台專案** ] 視窗中，按一下 [ **已啟用**]。 這會隱藏主控台中的所有專案。
5.  按一下 [選項] 面板中的 [ **顯示** ] 按鈕，以顯示允許的主控台專案清單。
6.  在開啟的 [ **顯示內容** ] 視窗中，于 [ **值** ] 資料行中輸入正式名稱。 請依需要重複步驟。
7.  按一下 [確定]。

如果您想要移除已新增至顯示或隱藏主控台專案清單中的所有專案，請返回步驟4中的畫面，然後選取 [ **未設定** ] 以清除清單。 如果您想要保留您的專案，但要暫止限制，請選取 [ **停用**]。

## <a name="remarks"></a>備註

您可能會在主控台中看到未列在其中的專案。 這些專案不是 Windows 的一部分，而是在安裝各種軟體和硬體時（例如 Microsoft Office 或視訊卡）新增。 非 Windows 的主控台專案不一定會有正式名稱。 若要找出此處未列出的主控台專案的正式名稱，請在下列路徑中查看登錄：

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

如需可協助您探索必要 Clsid 的詳細資訊，請參閱 [如何註冊可執行檔主控台專案](how-to-register-an-executable-control-panel-item-registration-.md) ，以及 [如何註冊 DLL 主控台專案](how-to-register-dll-control-panel-item-registration-.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[執行主控台專案](executing-control-panel-items.md)
</dt> <dt>

[**IOpenControlPanel**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



